<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body quote">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style>
.panel-body {
  font-family: "Arizonia", cursive;
  background: #f03c3c;
  font-size: 24px;
  color: #fff;
}

.quote {
  cursor: pointer;
}

.quote:hover {
  background-color: #fad200;
  color: #fff;
  font-size: 2.5rem;
  transform:rotate(-5deg);
  transition-delay: 0.2s;
  margin: 0.2rem;
  padding: 0.2rem;
}
</style>
