# 
```
var divE = document.createElement('div');
var divset = new Set();
for (var dk in divE) {
  divset.add(dk);
}
```

## Interface EventTarget
addEventListener
removeEventListener
dispatchEvent

## Interface Node : EventTarget
ELEMENT_NODE
ATTRIBUTE_NODE
TEXT_NODE
CDATA_SECTION_NODE
ENTITY_REFERENCE_NODE
ENTITY_NODE
PROCESSING_INSTRUCTION_NODE
COMMENT_NODE
DOCUMENT_NODE
DOCUMENT_TYPE_NODE
DOCUMENT_FRAGMENT_NODE
NOTATION_NODE

nodeType
nodeName
baseURI
isConnected
ownerDocument
parentNode
parentElement
hasChildNodes
childNodes
firstChild
lastChild
previousSibling
nextSibling
nodeValue
textContent

normalize
cloneNode
isEqualNode
isSameNode

DOCUMENT_POSITION_DISCONNECTED
DOCUMENT_POSITION_PRECEDING
DOCUMENT_POSITION_FOLLOWING
DOCUMENT_POSITION_CONTAINS
DOCUMENT_POSITION_CONTAINED_BY
DOCUMENT_POSITION_IMPLEMENTATION_SPECIFIC

compareDocumentPosition
contains
lookupPrefix
lookupNamespaceURI
isDefaultNamespace
insertBefore
appendChild
replaceChild
removeChild

## [Interface Element : Node](https://dom.spec.whatwg.org/#interface-element)
namespaceURI
prefix
localName
tagName
id
className
classList
slot
attributes
hasAttributes
getAttributeNames
getAttribute
getAttributeNS
setAttribute
setAttributeNS
removeAttribute
removeAttributeNS
hasAttribute
hasAttributeNS
toggleAttribute
getAttributeNode
getAttributeNodeNS
setAttributeNode
setAttributeNodeNS
removeAttributeNode
attachShadow
shadowRoot
closest
matches
webkitMatchesSelector
getElementsByTagName
getElementsByTagNameNS
getElementsByClassName
insertAdjacentElement
insertAdjacentText

## [interface HTMLElement : Element](https://html.spec.whatwg.org/multipage/dom.html#elements-in-the-dom)
title
lang
translate
dir
hidden
click
accessKey
draggable
spellcheck
autocapitalize
innerText
attachInternals

HTMLElement includes GlobalEventHandlers;
HTMLElement includes DocumentAndElementEventHandlers;
HTMLElement includes ElementContentEditable;
HTMLElement includes HTMLOrSVGElement;
HTMLElement includes ElementCSSInlineStyle;

### interface mixin GlobalEventHandlers 
onabort
onauxclick
onblur
oncancel
oncanplay
oncanplaythrough
onchange
onclick
onclose
oncontextmenu
oncuechange
ondblclick
ondrag
ondragend
ondragenter
ondragleave
ondragover
ondragstart
ondrop
ondurationchange
onemptied
onended
onerror
onfocus
oninput
oninvalid
onkeydown
onkeypress
onkeyup
onload
onloadeddata
onloadedmetadata
onloadstart
onmousedown
onmouseenter
onmouseleave
onmousemove
onmouseout
onmouseover
onmouseup
onmousewheel
onpause
onplay
onplaying
onprogress
onratechange
onreset
onresize
onscroll
onseeked
onseeking
onselect
onstalled
onsubmit
onsuspend
ontimeupdate
ontoggle
onvolumechange
onwaiting
onwheel

### interface mixin DocumentAndElementEventHandlers
oncopy
oncut
onpaste

### interface mixin ElementContentEditable
contentEditable
isContentEditable
enterKeyHint
inputMod


### interface mixin HTMLOrSVGElement
dataset
nonce
tabIndex
focus
blur

### [interface mixin ElementCSSInlineStyle](https://drafts.csswg.org/cssom-1/#elementcssinlinestyle)
style

## interface HTMLDivElement : HTMLElement
无


## 过时的属性
align


## 没有找到归属的属性
offsetParent
offsetTop
offsetLeft
offsetWidth
offsetHeight
outerText
ongotpointercapture
onlostpointercapture
onpointerdown
onpointermove
onpointerup
onpointercancel
onpointerover
onpointerout
onpointerenter
onpointerleave
onselectstart
onselectionchange
onformdata
onpointerrawupdate
part
assignedSlot
innerHTML
outerHTML
scrollTop
scrollLeft
scrollWidth
scrollHeight
clientTop
clientLeft
clientWidth
clientHeight
attributeStyleMap
onbeforecopy
onbeforecut
onbeforepaste
onsearch
previousElementSibling
nextElementSibling
children
firstElementChild
lastElementChild
childElementCount
onfullscreenchange
onfullscreenerror
onwebkitfullscreenchange
onwebkitfullscreenerror
setPointerCapture
releasePointerCapture
hasPointerCapture
insertAdjacentHTML
requestPointerLock
getClientRects
getBoundingClientRect
scrollIntoView
scroll
scrollTo
scrollBy
scrollIntoViewIfNeeded
animate
computedStyleMap
before
after
replaceWith
remove
prepend
append
querySelector
querySelectorAll
requestFullscreen
webkitRequestFullScreen
webkitRequestFullscreen
createShadowRoot
getDestinationInsertionPoints
elementTiming
getRootNode


