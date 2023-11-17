<template>
  <div class="py-4 container-fluid">
    <div class=" row">
      <div class="col-12 mb-5">
        <cars-table />
      </div>
      <div class="col-12">
        <nav aria-label="Page navigation example">
          <ul class="pagination">
            <li class="page-item">
              <a class="page-link" href="#" aria-label="Previous">
                <span aria-hidden="true">&laquo;</span>
                <span class="sr-only">Previous</span>
              </a>
            </li>
            <li class="page-item"><a class="page-link" href="#">1</a></li>
            <li class="page-item"><a class="page-link" href="#">2</a></li>
            <li class="page-item"><a class="page-link" href="#">3</a></li>
            <li class="page-item">
              <a class="page-link" href="#" aria-label="Next">
                <span aria-hidden="true">&raquo;</span>
                <span class="sr-only">Next</span>
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script>
    import CarsTable from "./components/CarsTable.vue";

    export default {
        name: "tables",
        components: {
            CarsTable,
        },
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
