## [Contributing](https://github.com/antoine92190/vue-advanced-chat/blob/master/.github/CONTRIBUTING.md)


## Named Slots

Example:

```javascript
<template #room-header="{ room, userStatus }">
  {{ room.roomName }} - {{ userStatus }}
</template>
```

| <div style="width:230px">Slot</div> | Action                                                      | Data                                | Overridden slots                                                                                                   |
| ----------------------------------- | ----------------------------------------------------------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| `room-texarea`                | Add a custom textarea |                                  |

## Slots original
### room-texarea
```
<textarea
  v-show="!file || imageFile || videoFile"
  ref="roomTextarea"
  v-model="message"
  :placeholder="textMessages.TYPE_MESSAGE"
  class="vac-textarea"
  :class="{
    'vac-textarea-outline': editedMessage._id
  }"
  :style="{
    'min-height': `${mediaDimensions ? mediaDimensions.height : 20}px`,
    'padding-left': `${
      mediaDimensions ? mediaDimensions.width - 10 : 12
    }px`
  }"
  @input="onChangeInput"
  @keydown.esc="escapeTextarea"
  @keydown.enter.exact.prevent=""
/>
```