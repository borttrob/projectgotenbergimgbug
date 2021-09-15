Calling the following in the failing folder doesn't render the image.

```
curl --request POST 'http://127.0.0.1:3000/forms/chromium/convert/html' \
--header 'Content-Type: multipart/form-data' \
--form 'files=@"index.html"' \
--form 'files=@"MyImg.png"' \
--form 'paperWidth="8.27"' \
--form 'paperHeight="11.7"' \
-o my.pdf
```

Whereas calling the following in the working folder works just fine.

```
curl --request POST 'http://127.0.0.1:3000/forms/chromium/convert/html' \
--header 'Content-Type: multipart/form-data' \
--form 'files=@"index.html"' \
--form 'files=@"myimg.png"' \
--form 'paperWidth="8.27"' \
--form 'paperHeight="11.7"' \
-o my.pdf
```
