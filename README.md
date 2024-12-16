# Video Downloader

`Video Downloader`는 YouTube, Instagram, TikTok에서 비디오, 오디오, 자막을 다운로드할 수 있는 Python 기반의 도구입니다. 이 도구는 `yt-dlp` 라이브러리를 사용하여 다양한 플랫폼에서 콘텐츠를 다운로드하고 메타데이터를 저장합니다.

## 설치

1. 이 저장소를 클론합니다:
   ```bash
   git clone https://github.com/hj0302/video-downloader.git
   cd video-downloader
   ```

2. 필요한 Python 패키지를 설치합니다:
   ```bash
   pip install -r requirements.txt
   ```

## 사용법

1. `example.ipynb` 노트북을 열고, `VideoDownloader` 클래스를 사용하여 콘텐츠를 다운로드합니다.

2. `VideoDownloader` 클래스 초기화:
   ```python
   downloader = VideoDownloader(base_dir='/path/to/downloads')
   ```

3. 콘텐츠 다운로드:
   - YouTube 비디오, 오디오, 자막 다운로드:
     ```python
     url = "https://www.youtube.com/watch?v=example"
     downloader.download_content(url, "youtube", "video")
     downloader.download_content(url, "youtube", "audio")
     downloader.download_content(url, "youtube", "subtitle")
     ```

   - Instagram 비디오 다운로드:
     ```python
     url = "https://www.instagram.com/reel/example/"
     downloader.download_content(url, "insta", "video")
     ```

   - TikTok 비디오 다운로드:
     ```python
     url = "https://www.tiktok.com/@username/video/example"
     downloader.download_content(url, "tiktok", "video")
     ```

## 디렉토리 구조

- `downloads/`: 다운로드된 콘텐츠가 저장되는 기본 디렉토리입니다.
  - `youtube/`: YouTube 콘텐츠 저장 디렉토리
    - `audio/`, `subtitle/`, `video/`, `metadata/`
  - `insta/`: Instagram 콘텐츠 저장 디렉토리
    - `video/`, `metadata/`
  - `tiktok/`: TikTok 콘텐츠 저장 디렉토리
    - `video/`, `metadata/`

## 주의사항

- 이 도구는 `yt-dlp` 라이브러리를 사용하므로, `ffmpeg`가 시스템에 설치되어 있어야 합니다.
- 다운로드한 콘텐츠는 개인적인 용도로만 사용해야 하며, 저작권을 준수해야 합니다.

## 기여

기여를 원하신다면, 이 저장소를 포크하고 풀 리퀘스트를 보내주세요. 버그 리포트나 기능 요청도 환영합니다.

## 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 `LICENSE` 파일을 참조하세요.