#!/bin/bash
# 定义源目录和目标文件路径
SOURCE_DIR="源目录地址"
TAR_FILE="目标文件路径"
current_date=$(date +%Y%m%d%H%M)
ENCRYPTED_FILE="备份路径"

# 使用 tar 压缩文件夹
echo "正在压缩文件夹 $SOURCE_DIR 到 $TAR_FILE..."
tar -cz -f "$TAR_FILE" "$SOURCE_DIR"

# 使用zip进行加密压缩,并备份
echo "正在压缩加密文件 $TAR_FILE 到 $ENCRYPTED_FILE..."
zip -r -Ppasswd "$ENCRYPTED_FILE" "$TAR_FILE"

# 删除打包文件
echo "删除未加密的压缩文件 $TAR_FILE..."
rm -vf "$TAR_FILE"

echo "操作完成，压缩并加密的文件存储在 $ENCRYPTED_FILE"
echo "$current_date"
