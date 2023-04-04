<script setup>
import AvatarExample from './avatar/examples/AvatarExample.vue'
import AvatarImageErrorHandlerExample from './avatar/examples/AvatarImageErrorHandlerExample.vue'
import AvatarBorderedExample from './avatar/examples/AvatarBorderedExample.vue'
import AvatarDotIndicatorExample from './avatar/examples/AvatarDotIndicatorExample.vue'
import AvatarSizeExample from './avatar/examples/AvatarSizeExample.vue'
import AvatarDotIndicatorPositionExample from './avatar/examples/AvatarDotIndicatorPositionExample.vue'
import AvatarAlternativeTextExample from './avatar/examples/AvatarAlternativeTextExample.vue'
import StackedAvatarsExample from './avatar/examples/StackedAvatarsExample.vue'
import AvatarPlaceholderExample from './avatar/examples/AvatarPlaceholderExample.vue'
import AvatarPlaceholderInitialsExample from './avatar/examples/AvatarPlaceholderInitialsExample.vue'

</script>
# Vue Avatar Component - Flowbite
Use the avatar component to show a visual representation of a user profile using an image element or SVG object based on multiple styles and sizes

## Default avatar
Use this example to create a circle and rounded avatar on an image element.

<AvatarExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>
<template>
    <div class="flex">
        <Avatar status="online" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" />
        <Avatar status="online" rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" />
    </div>
</template>
```

## Image Error Handler
Use this example to handle errors loading the `img` element, and display another `Avatar` instead.

<AvatarImageErrorHandlerExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
import { ref } from 'vue'

let imageError = ref(false)

function imageErrorHandler() {
    imageError.value = true
}
</script>
<template>
  <div class="vp-raw flex">
    <Avatar v-if="!imageError" status="online" img="https://flowbite.com/docs/images/people/profile-picture-not-found.jpg" @error:img="imageErrorHandler" />
    <Avatar v-else status="online" rounded />
  </div>
</template>
```

## Bordered
Use this example to create a circle and rounded avatar on an image element.

<AvatarBorderedExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>
<template>
    <div class="flex">
        <Avatar status="online" bordered img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
        <Avatar status="online" bordered rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    </div>
</template>
```

## Dot indicator
Use a dot element relative to the avatar component as an indicator for the user (eg. online or offline status).

<AvatarDotIndicatorExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>
<template>
    <div class="flex">
        <Avatar status="online" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
        <Avatar status="busy" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
        <Avatar status="away" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
        <Avatar status="offline" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    </div>
</template>
```

## Dot indicator position


<AvatarDotIndicatorPositionExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>
<template>
  <div class="flex items-center">
    <Avatar status="online" status-position="top-left" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="top-left" rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="top-right" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="top-right" rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="bottom-left" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="bottom-left" rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="bottom-right" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar status="online" status-position="bottom-right" rounded img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
  </div>
</template>
```

## Sizes

Choose from multiple sizing options for the avatar component from this example.

<AvatarSizeExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>
<template>
  <div class="flex items-center">
    <Avatar size="xs" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar size="sm" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar size="md" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar size="lg" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
    <Avatar size="xl" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" class="mr-2.5" />
  </div>
</template>
```

## Alternative text

<AvatarAlternativeTextExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>

<template>
    <Avatar status="online" alt="Alternative text" img="https://flowbite.com/docs/images/people/profile-picture-5.jpg"/>
</template>
```

## Stacked avatars
Use this example if you want to stack a group of users by overlapping the avatar components.

<StackedAvatarsExample />

```vue
<script setup>
import { StackedAvatars, Avatar, StackedAvatarsCounter } from 'flowbite-vue'
</script>

<template>
    <StackedAvatars>
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-1.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-2.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-3.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-4.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-5.jpg" rounded />
    </StackedAvatars>
    <StackedAvatars class="mt-2.5">
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-1.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-2.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-3.jpg" rounded />
      <Avatar stacked img="https://flowbite.com/docs/images/people/profile-picture-4.jpg" rounded />
      <StackedAvatarsCounter total="99" href="#" />
    </StackedAvatars>
</template>
```

## Placeholder icon

<AvatarPlaceholderExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>

<template>
  <div class="flex">
    <Avatar class="mr-2.5" />
    <Avatar rounded />
  </div>
</template>
```

## Placeholder initials

<AvatarPlaceholderInitialsExample />

```vue
<script setup>
import { Avatar } from 'flowbite-vue'
</script>

<template>
  <div class="flex">
    <Avatar initials="JD" class="mr-2.5" />
    <Avatar initials="JD" rounded />
  </div>
</template>
```
