<template>
  <section>
    <div>
      <h1>Button Default Stage</h1>
      <ButtonComponent />
    </div>
    <div>
      <h1>Button Variant = outline</h1>
      <ButtonComponent variant="outline" />
    </div>
    <div>
      <h1>Button Variant = text</h1>
      <ButtonComponent variant="text" />
    </div>
    <div>
      <h1>Button DisabledShadow</h1>
      <ButtonComponent disabledShadow />
    </div>

    <div>
      <h1>Button Disabled</h1>
      <ButtonComponent disabled />
    </div>
    <div>
      <h1>Button Disabled at variant = text</h1>
      <ButtonComponent disabled variant="text" />
    </div>

    <div>
      <h1>Button with starting icon</h1>
      <ButtonComponent startIcon="local_grocery_store" />
    </div>
    <div>
      <h1>Button with ending icon</h1>
      <ButtonComponent endIcon="local_grocery_store" />
    </div>

    <div>
      <h1>Button size = sm</h1>
      <ButtonComponent size="sm" />
    </div>
    <div>
      <h1>Button size = md</h1>
      <ButtonComponent size="md" />
    </div>
    <div>
      <h1>Button size = lg</h1>
      <ButtonComponent size="lg" />
    </div>

    <div>
      <h1>Button color = default</h1>
      <ButtonComponent color="default" />
    </div>
    <div>
      <h1>Button color = primary</h1>
      <ButtonComponent color="primary" />
    </div>
    <div>
      <h1>Button color = secondary</h1>
      <ButtonComponent color="secondary">secondary</ButtonComponent>
    </div>
    <div>
      <h1>Button color = danger</h1>
      <ButtonComponent color="danger" />
    </div>
  </section>
</template>

<script>
import ButtonComponent from "./components/ButtonComponent.vue";
export default {
  name: "App",
  components: {
    ButtonComponent,
  },
};
</script>
<style scoped>
section {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
}
div {
  margin: 20px;
}
</style>
