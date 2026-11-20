# up.sb Uploader

Upload a file to [up.sb](https://up.sb) from GitHub Actions.

## Run

1. Open the **Actions** tab.
2. Select **Upload files to up.sb**.
3. Choose **Run workflow**.
4. Enter a direct HTTP(S) file URL in `file_url`.
5. Optionally enter a destination name in `filename`.
6. Start the workflow and open its run summary to see the up.sb response.

The workflow downloads the file on the GitHub Actions runner, then uploads it using the command shown by up.sb:

```bash
curl https://up.sb -T your_file.txt
```

## Important

- The up.sb page states a maximum file size of 10 GB.
- Files are stored for 3 days and can be downloaded only once.
- The workflow currently accepts a direct HTTP(S) download URL; it does not yet accept a file attached directly to the workflow form.
- Treat the generated link as a one-time secret. Anyone who obtains it may be able to consume the download.
