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
1. Convert stream annotation type from `Audio` to `Sound`
1. posterCanvas
  - `posterCanvas` is deprecated
  - an `accompanyingCanvas` property is located inside the soundfile Canvas
  element
  - can more or less copy `posterCanvas` as an `accompanyingCanvas`.
  - no need for rendering proptery wihin accompanyingCanvas
1. there is a root level `rendering` property for "Download as PDF". Not needed,
   should be removed.
1. Annotations must have an `id` property
  - accompanyingCanvas -> items (AnnotationPage) -> items (Annotation)
  - Canvas[0] -> items (AnnotationPage) -> items (Annotation)
1. structures -> Range -> items -> Canvas elements don't need labels, and they are inorrectly structured.
