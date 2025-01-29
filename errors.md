## Validation errors encountered in Figgy generated IIIF Presentation V3
manifests


### Audio
1. Logo
  - logo property in the root document is deprecated
  - logo is instead located in an Agent provider
    ```
    "provider": [
        {
            "id": "https://library.princeton.edu",
            "type": "Agent",
            "label": {
                "en": [
                    "Princeton University Library"
                ]
            },
            "logo": [
                {
                    "id": "https://figgy-staging.princeton.edu/pul_logo_icon.png",
                    "type": "Image",
                    "format": "image/png",
                    "height": 100,
                    "width": 120
                }
            ]
        }
    ]
    ```
1. posterCanvas
  - posterCanvas is deprecated
  - Audio
    - an accompanyingCanvas property is located inside the soundfile Canvas
  - Video
    -
1. 
