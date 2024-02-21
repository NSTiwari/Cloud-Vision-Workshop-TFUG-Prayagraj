# Cloud Vision Workshop TFUG Prayagraj
Resources for Google Cloud workshop (TFUG Prayagraj) on using the Vision API.

Request body example:
echo '
{
  "requests": [
      {
        "image": {
          "source": {
              "gcsImageUri": "gs://YOUR_BUCKET_NAME/YOUR_IMAGE_NAME"
          }
        },
        "features": [
          {
            "type": "LABEL_DETECTION",
            "maxResults": 5
          }
        ]
      }
  ]
}
' > request.json

Hit Vision API request using curl.
`curl -s -X POST -H "Content-Type: application/json" --data-binary @request.json  https://vision.googleapis.com/v1/images:annotate?key=${API_KEY}`


