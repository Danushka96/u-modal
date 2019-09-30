<template>
<div class="v-overlay" style="z-index:201;">
  <div role="document" class="u-dialog__content" style="z-index: 9998;" tabindex="0">
    <div class="u-dialog" style="max-width: 600px;">
      <div class="u-card">
        <div class="u-card__title">
          <span class="headline">
            <slot name="title"></slot>
          </span>
        </div>
        <div class="u-card__text">
          <slot name="body"></slot>
        </div>
        <div class="u-card__actions">
          <div class="flex-grow-1"></div>
          <slot name="actions"></slot>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  props: {
    color: {
      type: String,
      default: "blue",
      validator(x) {
        return ["blue", "green", "red"].indexOf(x) !== -1;
      }
    },
    header: {
      type: String,
      default: "Header"
    },
    body: {
      type: String,
      default: "body"
    },
    footer: {
      type: String,
      default: "Footer"
    }
  }
};
</script>

<style scoped>
.v-overlay{
    font-size: 16px;
text-rendering: optimizeLegibility;
-webkit-font-smoothing: antialiased;
-webkit-tap-highlight-color: rgba(0, 0, 0, 0);
font-family: "Roboto", sans-serif;
line-height: 1.5;
box-sizing: inherit;
background-repeat: no-repeat;
padding: 0;
margin: 0;
align-items: center;
border-radius: inherit;
display: flex;
justify-content: center;
position: fixed;
top: 0;
left: 0;
right: 0;
bottom: 0;
transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1), z-index 1ms;
pointer-events: auto;
touch-action: none;
color: #FFFFFF;
z-index: 201;
}

.u-dialog__content {
  font-size: 16px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  line-height: 1.5;
  color: rgba(0, 0, 0, 0.87);
  box-sizing: inherit;
  background-repeat: no-repeat;
  padding: 0;
  margin: 0;
  align-items: center;
  display: flex;
  height: 100%;
  justify-content: center;
  left: 0;
  pointer-events: none;
  position: fixed;
  top: 0;
  transition: 0.2s cubic-bezier(0.25, 0.8, 0.25, 1), z-index 1ms;
  width: 100%;
  outline: none;
  z-index: 500;
}

.u-dialog {
  font-size: 16px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  line-height: 1.5;
  color: rgba(0, 0, 0, 0.87);
  box-sizing: inherit;
  background-repeat: no-repeat;
  padding: 0;
  border-radius: 4px;
  margin: 24px;
  overflow-y: auto;
  pointer-events: auto;
  transition: 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  width: 100%;
  z-index: inherit;
  box-shadow: 0px 11px 15px -7px rgba(0, 0, 0, 0.2),
    0px 24px 38px 3px rgba(0, 0, 0, 0.14), 0px 9px 46px 8px rgba(0, 0, 0, 0.12);
  max-height: 90%;
  max-width: 600px;
}

.u-card {
  font-size: 16px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  line-height: 1.5;
  pointer-events: auto;
  box-sizing: inherit;
  background-repeat: no-repeat;
  padding: 0;
  margin: 0;
  border-radius: 4px;
  display: block;
  max-width: 100%;
  outline: none;
  text-decoration: none;
  transition-property: box-shadow, opacity;
  overflow-wrap: break-word;
  position: relative;
  white-space: normal;
  transition: box-shadow 280ms cubic-bezier(0.4, 0, 0.2, 1);
  will-change: box-shadow;
  box-shadow: 0px 3px 1px -2px rgba(0, 0, 0, 0.2),
    0px 2px 2px 0px rgba(0, 0, 0, 0.14), 0px 1px 5px 0px rgba(0, 0, 0, 0.12);
  width: 100%;
  border-color: #ffffff;
  background-color: #ffffff;
  color: rgba(0, 0, 0, 0.87);
}

.u-card__title {
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  pointer-events: auto;
  overflow-wrap: break-word;
  white-space: normal;
  color: rgba(0, 0, 0, 0.87);
  box-sizing: inherit;
  background-repeat: no-repeat;
  margin: 0;
  align-items: center;
  display: flex;
  flex-wrap: wrap;
  line-height: 2rem;
  word-break: break-all;
  font-size: 1.25rem;
  font-weight: 500;
  letter-spacing: 0.0125em;
  padding: 16px 24px 10px;
  border-top-left-radius: inherit;
  border-top-right-radius: inherit;
}

.u-card__text {
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  pointer-events: auto;
  overflow-wrap: break-word;
  white-space: normal;
  box-sizing: inherit;
  background-repeat: no-repeat;
  margin: 0;
  font-size: 0.875rem;
  line-height: 1.375rem;
  letter-spacing: 0.0071428571em;
  color: rgba(0, 0, 0, 0.54);
  padding: 0 24px 20px;
}

.u-card__actions {
  font-size: 16px;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
  font-family: "Roboto", sans-serif;
  line-height: 1.5;
  pointer-events: auto;
  overflow-wrap: break-word;
  white-space: normal;
  color: rgba(0, 0, 0, 0.87);
  box-sizing: inherit;
  background-repeat: no-repeat;
  margin: 0;
  align-items: center;
  display: flex;
  padding: 8px;
  border-bottom-left-radius: inherit;
  border-bottom-right-radius: inherit;
  /* margin-left: 75%; */
  /* float: right; */
}
</style>