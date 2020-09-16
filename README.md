# youtube-dl-viewer

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).



# create needed dirs
`
mkdir -p /content/downloads
mkdir -p /content/videos
mkdir -p /static/v
`
# add a video
this downloads a video to the downloads folder inside content and then moves the json into the content folder for videos and the video file into the static serving folder
`
youtube-dl https://www.youtube.com/watch?v=NhVRB5sHteQ --write-info-json --write-thumbnail -o 'content/downloads/f%(format_id)s.%(ext)s'
mv content/downloads/*.json content/videos/
mv content/downloads/* static/v/
`