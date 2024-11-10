# YouTube Livestream Automation

This repository contains a GitHub Actions workflow for automated YouTube livestreaming.

## Setup Instructions

1. In your YouTube Studio, get your Stream Key and RTMP URL
2. Add these secrets to your GitHub repository:
   - Go to Settings > Secrets and Variables > Actions
   - Add two new secrets:
     - `YOUTUBE_RTMP_URL`: Your YouTube RTMP URL
     - `YOUTUBE_STREAM_KEY`: Your YouTube Stream Key

## Usage

1. Go to the Actions tab in your repository
2. Select "YouTube Live Stream Workflow"
3. Click "Run workflow"
4. Enter the URL of the video you want to stream
5. Click "Run workflow"

## FFmpeg Configuration

The workflow uses FFmpeg with these settings:
- Video: H.264 codec with 3000kbps bitrate
- Audio: AAC codec with 160kbps bitrate
- Keyframe interval: 50 frames
- Preset: veryfast for optimal streaming performance

## Security Notes

- Never commit your YouTube stream key or RTMP URL directly in the code
- Always use GitHub Secrets for sensitive credentials
- Regularly rotate your stream key for security
