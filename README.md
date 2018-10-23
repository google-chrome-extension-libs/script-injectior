# script-injectior
inject script into a page , without duplicates 

### Mechanics

- background.js 
  - Listen: [inject] message
    - send [wannascript] message to an active tab
      - silence means consent
      - answer means no, if:
         - answer[page_url] = active tab url
- content.js
  - Listen: [wannascript] message
    - answer, if you can, with props: (page_url)
- event initiator(popup.js by default)
  - emmit: [inject] message
