<template>
  <div class="navbar navbar-expand-sm navbar-light navbar-lewagon">
    <a class="navbar-brand" href="#">
      <img alt="Einhorn" :src="unicornUrl" />
    </a>
    <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Der Autor</a>
        </li>
        <li class="nav-item dropdown">
          <img class="avatar dropdown-toggle" id="navbarDropdown" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false" :src="author.image" />
          <div class="dropdown-menu dropdown-menu-right" aria-labelledby="navbarDropdown">
            <a class="dropdown-item" href="#">Action</a>
            <a class="dropdown-item" href="#">Another action</a>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    author: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      /* eslint-disable global-require */
      unicornUrl: require('@/assets/einhorn.svg'),
      /* eslint-enable global-require */
    };
  },
}
</script>

<style>
.navbar-lewagon {
  justify-content: space-between;
  background: white;
}

.navbar-lewagon .navbar-collapse {
  flex-grow: 0;
}

.navbar-lewagon .navbar-brand img {
  width: 40px;
}

.avatar {
  width: 40px;
  border-radius: 50%;
}

.avatar-large {
  width: 56px;
  border-radius: 50%;
}

.avatar-bordered {
  width: 40px;
  border-radius: 50%;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}

.avatar-square {
  width: 40px;
  border-radius: 0px;
  box-shadow: 0 1px 2px rgba(0,0,0,0.2);
  border: white 1px solid;
}
</style>