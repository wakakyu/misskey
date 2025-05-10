<!--
SPDX-FileCopyrightText: syuilo and misskey-project
SPDX-License-Identifier: AGPL-3.0-only
-->

<template>
<span>
	<span>@{{ user.username }}</span>
	<span v-if="(user.username === 'RinK') && (user.host === 'i.wakakyu.net' || host === 'i.wakakyu.net')">@i<span style="opacity: 0.5;">.wakakyu.net</span></span>
	<span v-else-if="user.host || detail" style="opacity: 0.5;">@{{ user.host || host }}</span>
</span>
</template>

<script lang="ts" setup>
import * as Misskey from 'misskey-js';
import { toUnicode } from 'punycode.js';
import { host as hostRaw } from '@@/js/config.js';

defineProps<{
	user: Misskey.entities.UserLite;
	detail?: boolean;
}>();

const host = toUnicode(hostRaw);
</script>
