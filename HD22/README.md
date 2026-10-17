# HD22 高分辨率彩色图像测试集

本仓库发布用于图像去噪评估的 22 张高分辨率彩色图像。图像来自摄影展采集。依据发布者确认的授权，本版本公开再分发图像；按授权要求不列摄影者姓名。发布副本已移除 EXIF、XMP、IPTC、PNG 文本等描述性元数据，图像解码后的像素值与来源文件逐像素一致。manifest.csv 提供文件名、尺寸、格式、字节数和 SHA-256 校验值。

数据集共 22 张图像，约 44.8 MB，尺寸范围为 999×999 至 3500×3500 像素。论文实验对 RGB 通道分别添加标准差为 15、25、50、80（8 位像素尺度）的加性高斯白噪声；本仓库只含干净图像。

## 使用与引用

论文引用：HD22 高分辨率彩色图像测试集（版本 1.0，2026）。正式版本目录：https://github.com/18211900623/erduoxiucifangfa/tree/v1.0.0/HD22

图像依发布者取得的公开再分发授权提供。本仓库不授予超出该授权范围的额外许可；使用者应遵守适用的授权条件。仓库未附加独立的 CC 或其他开放数据许可证。

## 校验

运行 sha256sum -c manifest.sha256 可核对图像文件。逐文件 SHA-256 也列在 manifest.csv 中。

---

# HD22 High-Resolution Color Image Test Set

This repository contains 22 high-resolution color images used for image-denoising evaluation. The images were collected from a photography exhibition. Under the redistribution authorization confirmed by the depositor, the files are publicly redistributed without photographer names. Descriptive EXIF, XMP, IPTC, and PNG text metadata have been removed from the release copies; decoded pixel values are identical to the source files. manifest.csv lists filenames, dimensions, format, byte size, and SHA-256 checksums.

The dataset contains 22 images (about 44.8 MB), sized from 999×999 to 3500×3500 pixels. The experiments add AWGN independently to RGB channels at standard deviations 15, 25, 50, and 80 on the 8-bit scale. Only clean images are included.

Images are provided under the depositor's public redistribution authorization. This repository does not grant additional permissions beyond that authorization and does not attach a separate CC or other open-data license.

