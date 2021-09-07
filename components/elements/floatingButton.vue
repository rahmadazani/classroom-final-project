<template>
  <div>
    <div id="floating-button" class="btn-group dropup">
      <button
        class="btn btn-primary dropdown-toggle"
        data-toggle="dropdown"
        aria-haspopup="true"
        aria-expanded="false"
        type="button"
      >
        <i class="fas fa-plus"></i>
      </button>
      <div class="dropdown-menu">
        <a
          class="dropdown-item"
          href="#"
          data-toggle="modal"
          data-target="#formClass"
          >Add Class</a
        >
      </div>
    </div>

    <div
      class="modal fade"
      data-backdrop="false"
      id="formClass"
      tabindex="-1"
      aria-labelledby="exampleModalLabel"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel">Formulir Kelas</h5>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            <input type="text" />
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-dismiss="modal"
            >
              Close
            </button>
            <button type="button" class="btn btn-primary">Join Kelas</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
#floating-button {
  position: fixed;
  bottom: 3em;
  right: 3em;
  z-index: 10000;
}
</style>