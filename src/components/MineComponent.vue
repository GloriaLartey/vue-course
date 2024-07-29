<script setup>
const vFormateDiv = {
  mounted: (el, binding) => {
    //console.log(el)
    // el.style.fontSize = binding.value + 'px'
    el.style.fontSize = '3rem'
    el.style.fontStyle = 'italic'
    // el.style.color = 'teal'
    // el.style.border = `${binding.value}px solid teal`

    switch (binding.arg) {
      case 'orange':
        el.style.color = 'orange'
        break
      case 'pink':
        el.style.color = 'pink'
        break
      case 'purple':
        el.style.color = 'purple'
        break
      case 'teal':
        el.style.color = 'teal'
        break
      default:
        el.style.color = 'black'
    }
  }
}

// const vFormateDiv = (el) => el.style.fontSize = '5rem'
</script>

<template>
  <div v-formate-div:orange>Using simple custom directive</div>
  <div v-formate-div:pink>Using simple custom directive</div>
  <div v-formate-div:purple>Using simple custom directive</div>
  <div v-formate-div:teal>Using simple custom directive</div>
  <div v-formate-div:>Using simple custom directive</div>

  <div v-formate-div>Riason</div>
</template>
