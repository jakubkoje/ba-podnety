<template>
	<ion-page>
		<ion-header>
			<ion-toolbar>
				<ion-title>Bratislava</ion-title>
			</ion-toolbar>
		</ion-header>
		<ion-content>
			<Podnet name="Tab 1 page" />
		</ion-content>
	</ion-page>
</template>

<script lang="ts">
import {
	IonPage,
	IonHeader,
	IonToolbar,
	IonTitle,
	IonContent,
} from '@ionic/vue';
import Podnet from '@/components/Podnet.vue';

export default {
	name: 'Tab1',
	components: {
		Podnet,
		IonHeader,
		IonToolbar,
		IonTitle,
		IonContent,
		IonPage,
	},
};
</script>