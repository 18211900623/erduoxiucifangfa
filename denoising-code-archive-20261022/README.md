# FORD denoising source archive

This directory contains the complete Git bundle for the denoising source archive, split into numbered 24,000-byte parts so it can be stored through GitHub's file API.

The bundle preserves the source repository's Git history and includes the reproducibility scripts and historical implementations prepared for the paper. It does not include image datasets or generated experiment outputs.

## Restore on Windows

Download this repository branch, then run PowerShell from the downloaded repository root:

```powershell
$parts = Get-ChildItem .\denoising-code-archive-20261022\source-history.bundle.part* | Sort-Object Name
$out = [IO.File]::Create((Join-Path (Get-Location) 'source-history.bundle'))
try {
  foreach ($part in $parts) {
    $input = [IO.File]::OpenRead($part.FullName)
    try { $input.CopyTo($out) } finally { $input.Dispose() }
  }
} finally { $out.Dispose() }

(Get-FileHash .\source-history.bundle -Algorithm SHA256).Hash
git clone .\source-history.bundle .\FORD-source-history
```

The SHA-256 of the reconstructed bundle must be:

`453EDFD95AC510529F97A63848CAA29D73BF733617457CDA004B5B8E83BA21FC`

The local bundle was verified with `git bundle verify` before upload.
