<template>
  <div class="py-4 container-fluid">
    <div class=" row">
      <div class="col-md-8">
        <div class="card">
          <div class="card-header pb-0">
            <div class="d-flex align-items-center">
              <p class="mb-0">Редагування інформації про траспорт</p>
              <argon-button color="success" size="sm" class="ms-auto">Settings</argon-button>
            </div>
          </div>
          <div class="card-body">
            <p class="text-uppercase text-sm">Загальна Інформація</p>
            <div class="row">
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label">Категорія транспортного засобу</label>
                <div class="form-group">
                  <select id="categories" name="category_id" data-field="category" aria-label="Тип транспорту" data-placeholder="Будь-який" class="form-select">
                    <option value="0">Будь-який</option>
                    <option selected="selected" value="1">Легкові</option>
                    <option value="2">Мото</option>
                    <option value="6">Вантажівки</option>
                    <option value="5">Причепи</option>
                    <option value="4">Спецтехніка</option>
                    <option value="10">Сільгосптехніка</option>
                    <option value="7">Автобуси</option>
                    <option value="3">Водний транспорт</option>
                    <option value="9">Повітряний транспорт</option>
                    <option value="8">Автобудинки</option>
                  </select>
                </div>
              </div>
            </div>
            <div class="row">
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label"
                >Марка</label
                >
                <argon-input type="text" value="Huyndai" />
              </div>
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label"
                >Модель</label
                >
                <argon-input type="text" value="Elantra" />
              </div>
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label"
                >Рік випуску</label
                >
                <argon-input type="text" value="2013" />
              </div>
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label"
                >Колір</label
                >
                <argon-input type="text" value="Чорний" />
              </div>
            </div>
            <hr class="horizontal dark" />
            <p class="text-uppercase text-sm">Реєстраційні дані</p>
            <div class="row">
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label">Держ. номер</label>
                <argon-input type="text" value="ВМ7660СТ" />
              </div>
              <div class="col-md-6">
                <label for="example-text-input" class="form-control-label">VIN КОД</label>
                <argon-input type="text" value="KMHDH41CADU905568" />
              </div>
              <div class="col-md-4">
                <label for="example-text-input" class="form-control-label">Дата реєстрації</label>
                <argon-input type="text" value="26.11.2021" />
              </div>
              <div class="col-md-4">
                <label for="example-text-input" class="form-control-label"
                >Postal code</label
                >
                <argon-input type="text" value="437300" />
              </div>
            </div>
            <hr class="horizontal dark" />
            <p class="text-uppercase text-sm">About me</p>
            <div class="row">
              <div class="col-md-12">
                <label for="example-text-input" class="form-control-label"
                >About me</label
                >
                <argon-input
                        type="text"
                        value="A beautiful Dashboard for Bootstrap 5. It is Free and Open Source."
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-4">
        <vehicle-card />
      </div>
    </div>
  </div>
</template>

<script>
    //import setNavPills from "@/assets/js/nav-pills.js";
    //import setTooltip from "@/assets/js/tooltip.js";
    import VehicleCard from "./components/VehicleCard.vue";
    import ArgonInput from "@/components/ArgonInput.vue";
    import ArgonButton from "@/components/ArgonButton.vue";

    export default {
        name: "tables",
        components: { VehicleCard, ArgonInput, ArgonButton },
        data() {
            return {
                stats: {
                    titleColor: "opacity-7 text-white",
                    descColor: "text-white",
                    trip: {
                        title: "Today's Trip",
                        desc: "145 KM",
                        classIcon: "text-dark ni ni-money-coins",
                    },
                    health: {
                        title: "Battery Health",
                        desc: "99 %",
                        classIcon: "text-dark ni ni-controller ",
                    },
                    speed: {
                        title: "Average Speed",
                        desc: "56 Km/h",
                        classIcon: "text-dark ni ni-delivery-fast",
                    },
                    volume: {
                        title: "Music Volume",
                        desc: "15/100",
                        classIcon: "text-dark ni ni-note-03",
                    },
                },
            };
        },
    };
</script>
