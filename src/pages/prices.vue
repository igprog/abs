<template>
  <div class="container py-5">
    <h2 class="pt-5">{{ $t('prices') }}</h2>
    <div class="row">
      <div class="col-sm-6">
        <div class="table-responsive">
            <table class="table table-bordered shadow">
              <tr>
                <th class="bg-light">{{ $t('month') }}</th>
                <th class="bg-light">{{ $t('price') }}</th>
              </tr>
              <tr>
                <td>7 {{ $t('and') }} 8</td>
                <td>250 €</td>
              </tr>
              <tr>
                <td>6 {{ $t('and') }} 9</td>
                <td>220 €</td>
              </tr>
              <tr>
                <td>5 {{ $t('and') }} 10</td>
                <td>180 €</td>
              </tr>
            </table>
          </div>
      </div>
      </div>
    </div>
</template>

<script>
export default {
  metaInfo: {
    titleTemplate: "%s | Cijene",
    meta: [
      {
        name: "description",
        content:
          "Apartment Bepina - Cijene",
      },
    ],
  },
};
</script>
