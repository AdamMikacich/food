<template>
  <div class="list">
    <h2 class="subtitle">Attendees</h2>
    <ul id="attendees">
      <!-- Create a list element for each user and display whether they are gluten free, vegan, both, or neither -->
      <li v-for="(attendee, index) in $store.getters.currentEvent.attendees" :key="'attendee' + index">
        {{ attendee.name }}
        <span class="blue">
          {{ attendee.gf ? '(Gluten Free)' : '' }}
        </span>
        <span class="green">
          {{ attendee.v ? '(Vegan)' : '' }}
        </span>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style>
#attendees {
  list-style-type: circle;
  padding-left: 20px;
}

span.blue {
  color: #56a7ff;
}

span.green {
  color: #44bd32;
}
</style>