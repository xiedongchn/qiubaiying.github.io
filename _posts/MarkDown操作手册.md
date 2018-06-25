###插入图片

![tt](tt.png)

##### 插入图片要诀：shell中执行"openssl base64 -in \<infile> -out \<outfile>"，获取图片的base64编码，使用命令"<!\[avatar][photo]>"引用图片的base64编码即可显示图片([photo]:data:image/png;base64,iVBORw0...)