# Kick Stream Recorder - pb7live

Automated 24/7 cloud recorder for Kick channel **[pb7live](https://kick.com/pb7live)**.

### Features:
- **Cloudflare Bypass:** Uses `curl_cffi` (impersonate Chrome) with Netscape cookies to detect live streams reliably.
- **High-Quality Capture:** Captures stream with HLS / ffmpeg in `.ts` format at 720p/1080p.
- **Continuous Multi-Shift Coverage:** 3 consecutive shifts per day (~13 hours total coverage) with auto-continuation.
- **Dual Cloud Storage:** Uploads to Gofile.io with direct download links and saves GitHub Actions artifacts.

### Manual Dispatch:
```bash
gh workflow run record.yml --repo gauravdev833844-gif/kick-pb7live -f hours=4.5 -f shifts_left=2 -f always_continue=true
```
