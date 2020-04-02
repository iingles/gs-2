<template>
  <div id="app">
    <div class="container-fluid container-tw">
      <div class="container">
        <h1>Twitter Clone</h1>
      </div>
    </div>

    <div class="container-fluid container-tw">
      <div class="container">
        <div class="row">
          <section class="col-sm-12 col-md-6 col-lg-8 main-content">
            <h4>Main Content</h4>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc non arcu at sapien
              interdum dignissim eu ac nisi. Duis ante nunc, mattis volutpat lectus id, mollis
              tincidunt orci. Mauris vitae lorem nisi. Fusce a mollis lorem. Duis blandit est
              libero, in convallis massa aliquam ut. In mollis eleifend nibh, eu commodo enim
              ullamcorper fermentum. Quisque eleifend quam vitae lectus luctus pulvinar.
              Quisque euismod ultrices maximus. Quisque facilisis vestibulum nisi quis mollis.
              Curabitur in nulla turpis. Donec ornare facilisis placerat. Nullam non dolor
              aliquet, pulvinar nunc vitae, aliquam massa. Integer volutpat arcu eu ante
              rhoncus faucibus. Nullam ornare euismod sollicitudin. Quisque lacus ante, cursus
              ac vulputate sit amet, commodo ut odio. Ut egestas eleifend massa, at mollis
              nulla ullamcorper sed.
            </p>
          </section>
          <div class="col-sm-12 col-md-6 col-lg-4">
            <div class="side-content">
              Side Content
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
@twblue: #15202B;
@twgray: #CCD6DD;

h1 {
  font-size: 2rem;
}

p {
  font-size: 1rem;
}

.container-tw {
  background: @twblue;
  color: #fff;
  border-bottom: 1px solid @twgray;
}

.container {
  max-width: 990px;
}

.main-content {
  border-left: 1px
  solid @twgray;
  border-right: 1px solid @twgray;
  padding: 20px;
}

.side-content {
  border: 1px solid @twgray;
  border-radius: 10px;
  margin: 20px 10px;
  padding:20px;
}

</style>
