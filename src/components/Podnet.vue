<template>
	<div id="container">
		<ion-card>
			<img
				src="https://www.odkazprestarostu.sk/image/w1280/public/alerts/85005/images/5e26d68f01282.jpg"
				class="ion-padding-top ion-padding-horizontal"
			/>
			<ion-card-header>
				<ion-badge color="warning" class="mr-2">Ruzinov</ion-badge>
				<ion-badge color="success">Vyriesene</ion-badge>
				<ion-card-title
					>Námestie SNP - osvetlenie - nedostatočné</ion-card-title
				>
			</ion-card-header>
			<ion-card-content style="display: flex" class="ion-align-items-center">
				<ion-label slot="start" class="flex1">Námestie SNP</ion-label>
				<ion-buttons slot="end" class="flex2">
					<ion-button @click="like()">
						<ion-icon
							class="like-icon"
							slot="icon-only"
							:icon="isLiked ? thumbsUp : thumbsUpOutline"
							color="success"
						></ion-icon>
					</ion-button>
					<ion-label>{{ likeCount }}</ion-label>
				</ion-buttons></ion-card-content
			>
		</ion-card>
	</div>
</template>

<script>
import {
	IonCard,
	IonCardContent,
	IonCardTitle,
	IonCardHeader,
	IonBadge,
	IonButtons,
	IonButton,
	IonIcon,
	IonLabel,
} from '@ionic/vue';

import { thumbsUp, thumbsUpOutline } from 'ionicons/icons';
export default {
	name: 'ExploreContainer',
	components: {
		IonCard,
		IonCardContent,
		IonCardTitle,
		IonCardHeader,
		IonBadge,
		IonButtons,
		IonButton,
		IonIcon,
		IonLabel,
	},
	data() {
		return {
			isLiked: false,
			likeCount: 0,
			thumbsUpOutline,
			thumbsUp,
		};
	},
	methods: {
		like() {
			this.isLiked = !this.isLiked;
			if (this.isLiked) {
				this.likeCount++;
			} else {
				this.likeCount--;
			}
		},
	},
};
</script>

<style scoped>
.mr-2 {
	margin-right: 0.5rem;
}
ion-card-title {
	margin-top: 0.8rem;
	font-size: 1.5rem;
}
.flex1 {
	flex: 1;
	height: 100%;
}
.flex2 {
	flex: 0.1;
}
like-icon {
	color: var(--ion-color-success);
}
</style>