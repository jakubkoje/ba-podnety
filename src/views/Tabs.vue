<template>
	<ion-page>
		<ion-tabs>
			<ion-tab-bar slot="bottom">
				<ion-tab-button tab="tab1" href="/tabs/tab1">
					<ion-icon :icon="homeOutline" />
					<ion-label>Bratislava</ion-label>
				</ion-tab-button>

				<ion-tab-button tab="tab2" href="/tabs/tab2" disabled>
					<ion-icon :icon="personCircleOutline" />
					<ion-label>Moje podnety</ion-label>
				</ion-tab-button>

				<ion-tab-button tab="tab3" href="/tabs/tab3" disabled>
					<ion-icon :icon="addCircleOutline" />
					<ion-label>Pridať podnet</ion-label>
				</ion-tab-button>
			</ion-tab-bar>
		</ion-tabs>
	</ion-page>
</template>

<script lang="ts">
import {
	IonTabBar,
	IonTabButton,
	IonTabs,
	IonLabel,
	IonIcon,
	IonPage,
} from '@ionic/vue';
import {
	ellipse,
	square,
	triangle,
	addCircleOutline,
	personCircleOutline,
	homeOutline,
} from 'ionicons/icons';

export default {
	name: 'Tabs',
	components: { IonLabel, IonTabs, IonTabBar, IonTabButton, IonIcon, IonPage },
	setup() {
		return {
			ellipse,
			square,
			triangle,
			addCircleOutline,
			personCircleOutline,
			homeOutline,
		};
	},
};
</script>