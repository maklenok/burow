<template>
<div class="cover-container d-flex w-100 h-100 p-3 mx-auto flex-column">

<main class="px-3">
  <h1>Сайт Сергея Бабатчикова</h1>
  <p class="lead">Уроженец Новосибирска, студент ВКИ НГУ</p>
</main>
<div class="container">

    <v-simple-table dark>
      <template v-slot:default>
        <thead>
        <tr>
          <th class="text-left">
            Время
          </th>
          <th class="text-left">
            Занятие
          </th>
        </tr>
        </thead>
        <tbody>
        <tr
            v-for="item in time"
            :key="item.name"
        >
          <td>{{ item.employment }}</td>
          <td>{{ item.name}}</td>
        </tr>
        </tbody>
      </template>
    </v-simple-table>

</div>
</div>
</template>


<script>
export default {
  data () {
    return {
      time: [
        {
          name: 'Подъём',
          employment: '7:30',
        },
        {
          name: 'Завтрак',
          employment: '7:40',
        },
        {
          name: 'Шкила',
          employment: '8:00',
        },
        {
          name: 'Уроки',
          employment: '14:00',
        },
        {
          name: 'Игра в компик',
          employment: '14:00',
        },
        {
          name: 'Ванна',
          employment: '20:00',
        },
        {
          name: 'Спать',
          employment: '21:00',
        },
      ],
    }
  },
}
</script>