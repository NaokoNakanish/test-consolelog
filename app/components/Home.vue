<template>
    <Page>
        <ActionBar>
            <Label text="Home"/>
        </ActionBar>

        <GridLayout>
            <Label class="info">
                <FormattedString>
                    <Span class="fas" text.decode="&#xf135; "/>
                    <Span :text="message" @tap="hello"/>

                </FormattedString>
            </Label>
        <Button text="Button" @tap="onButtonTap" />
        </GridLayout>
    </Page>
</template>

<script>
  export default {
      data() {
          return {
              bango: 0
          }
      },
    computed: {
        
      message() {
          console.log('hello')
        return "Blanaaak {N}-Vue app";
      }
    },
    methods: {
        onButtonTap() {
            console.log("taptap")
        },
        hello() {
            console.log('hello')
        }
    }
  };
</script>

<style scoped lang="scss">
    @import '@nativescript/theme/scss/variables/blue';

    // Custom styles
    .fas {
        @include colorize($color: accent);
    }

    .info {
        font-size: 20;
        horizontal-align: center;
        vertical-align: center;
    }
</style>
