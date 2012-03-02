s3cacher
--------

This WSGI app takes files from a source URL, and stores them in S3. If placed behind Nginx/Varnish,
this can be used to achieve the following logic:
    
* Image request is received
* If the image is already in S3, serve it from there
* If not, get the image from the source, and store it in S3 so it can be served directly on the
    next request
