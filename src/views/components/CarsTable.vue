<template>
  <div class="card">
    <div class="card-header pb-0">
      <h6>Мої транспортні засоби</h6>
    </div>
    <div class="card-body px-0 pt-0 pb-2">
      <div class="table-responsive p-0">
        <table class="table align-items-center mb-0">
          <thead>
            <tr>
              <th class="text-uppercase text-secondary text-xxs font-weight-bolder opacity-7">Модель</th>
              <th class="text-uppercase text-secondary text-xxs font-weight-bolder opacity-7 ps-2">Держ. номер</th>
              <th class="text-center text-uppercase text-secondary text-xxs font-weight-bolder opacity-7">VIN код</th>
              <th class="text-center text-uppercase text-secondary text-xxs font-weight-bolder opacity-7">Реєстрація</th>
              <th class="text-center text-uppercase text-secondary text-xxs font-weight-bolder opacity-7">Статус</th>
              <th class="text-secondary opacity-7"></th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>
                <div class="d-flex px-2 py-1">
                  <div>
                    <img
                      src="https://cdn.riastatic.com/photosnewr/auto/photo/hyundai-elantra__333540270-460x345.webp"
                      class="avatar avatar-sm me-3"
                      alt="user1"
                    />
                  </div>
                  <div class="d-flex flex-column justify-content-center">
                    <h6 class="mb-0 text-sm">HYUNDAI</h6>
                    <p class="text-xs text-secondary mb-0">ELANTRA</p>
                  </div>
                </div>
              </td>
              <td>
                <p class="text-xs font-weight-bold mb-0 ">ВМ7660СТ</p>
              </td>
              <td class="align-middle text-center">
                <p class="text-xs font-weight-bold mb-0">KMHDH41CADU905568</p>
              </td>
              <td class="align-middle text-center text-sm">
                <p class="text-xs text-secondary mb-0">26.11.2021</p>
              </td>
              <td class="align-middle text-center">
                <span class="badge badge-sm bg-gradient-primary">Використовується</span>
              </td>
              <td class="align-middle">
                <a href="/my-garage/edit"
                  class="text-secondary font-weight-bold text-xs"
                >Edit</a>
              </td>
            </tr>
            <tr>
              <td>
                <div class="d-flex px-2 py-1">
                  <div>
                    <img
                            src="https://cdn.riastatic.com/photosnewr/auto/new_auto_storage/bajaj-pulsar__2099107-620x465x72.webp"
                            class="avatar avatar-sm me-3"
                            alt="user1"
                    />
                  </div>
                  <div class="d-flex flex-column justify-content-center">
                    <h6 class="mb-0 text-sm">HYUNDAI</h6>
                    <p class="text-xs text-secondary mb-0">ELANTRA</p>
                  </div>
                </div>
              </td>
              <td>
                <p class="text-xs font-weight-bold mb-0 ">ВМ7660СТ</p>
              </td>
              <td class="align-middle text-center">
                <p class="text-xs font-weight-bold mb-0">KMHDH41CADU905568</p>
              </td>
              <td class="align-middle text-center text-sm">
                <p class="text-xs text-secondary mb-0">26.11.2021</p>
              </td>
              <td class="align-middle text-center">
                <span class="badge badge-sm bg-gradient-primary">Використовується</span>
              </td>
              <td class="align-middle">
                <a href="/my-garage/edit"
                   class="text-secondary font-weight-bold text-xs"
                >Edit</a>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "cars-table",
};
</script>
