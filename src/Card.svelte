<ion-card>
  <ion-card-content>
    <slot name="content"><!-- optional fallback --></slot>
    <ion-grid>
      <ion-row>
        <ion-col>
          <ion-button size="small" on:click>เข้าชม</ion-button>
        </ion-col>
        <ion-col>
          <ion-button fill="clear">
            <ion-icon slot="icon-only" name="heart-outline" />
          </ion-button>
          <ion-button fill="clear">
            <ion-icon slot="icon-only" ios="share-outline" md="share-outline" />
          </ion-button>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-card-content>
</ion-card>
