# This is a fork of level3tjg's decryptedappstore-action to add the version to the IPA's file name. May be useful for those who want to automate an AltStore source :)

## Inputs
```yaml
inputs:
  appstore_url:
    description: AppStore URL for the app you want to download
    required: true
    type: string
  cache:
    description: Cache downloaded IPAs
    default: true
    type: boolean
  path:
    description: Path to download the ipa to
    type: string
  token:
    description: Your decryptedappstore session token
    required: true
    type: string
  version:
    description: Version of the app to download
    default: latest-available
    type: string
```

## Example

```yaml
steps:
  - name: Download IPA
    uses: MrZomka/daa-withversion@main
    with:
      appstore_url: "https://apps.apple.com/us/app/youtube-watch-listen-stream/id544007664"
      path: App.ipa
      token: "${{ secrets.SESSION_TOKEN }}"
```
