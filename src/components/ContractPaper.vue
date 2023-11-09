<template>
  <div style="display: flex; gap: 20px">
    <div>

      <button class="show-paper" @click="showA4Page">
      <span>Посмотреть договор</span>
      <q-icon class="main-contract-expand" :name="expandIcon"></q-icon>
    </button>
    <div  v-if="showPaper">
  <div class="a4-page">
    <div class="content">
      <div class="page-text">
        <h5>Договор предоплаты купли-продажи набора кухонной мебели</h5>
        <div style="display: flex; justify-content: space-between; margin-bottom: 10px">
        <span> г. Алматы </span>

          <div style="display: flex; gap: 5px">
          <span id="day"> «{{day}}» </span>
          <span id="month"> {{ month }} </span>
            <span id="dayOfWeek">{{ dayOfWeek }}</span>
            <span id="year">2023 г.</span>
          </div>

        </div>


        <p><span style="font-weight: bold">ТОО «Test»</span> в лице директора Иванов Иван, действующего на основании Устава, именуемое в дальнейшем «Продавец», с одной стороны, и гр. {{fullName}} уд.личности: №
          {{ udostakNumber }}, выданный {{ udostakDate }}, проживающий по адресу:
          {{ livingIn }}, именуемый в дальнейшем «Покупатель», с другой стороны, заключили настоящий Договор предоплаты о нижеследующем:</p>

        <h6> 1.	ПРЕДМЕТ ДОГОВОРА. </h6>
        <p>1.1. Продавец обязуется передать в собственность Покупателя набор мебели для кухни (далее «Товар»), а Покупатель обязуется принять Товар и уплатить Продавцу за него денежную сумму, в порядке и размере, предусмотренных Договором.</p>
        <p>1.2. Предметом Договора является Товар, заказанный Покупателем и соответствующий описанию, предусмотренного Приложением №1 к Основному Договору;</p>
        <p>1.3. Покупателю могут быть предоставлены дополнительные услуги по замеру помещения, установке (монтажу) и доставке Товара: {{dopUslugi}}</p>
        <p>1.3.1. стоимость Услуг не включается в стоимость Товара. Указанные услуги предоставляются Покупателю только при условии приобретения Товара.</p>


        <h6>2. ПОРЯДОК ИСПОЛНЕНИЯ ДОГОВОРА</h6>
        <p>2.1. Покупатель, ознакомившись с демонстрируемыми образцами, потребительскими свойствами и условиями поставки, заказывает необходимый ему Товар и заключает Договор предоплаты. При этом, стороны в дальнейшем обязуются заключить Основной Договор купли-продажи кухонного набора (далее «Основной Договор»).</p>


        <h6>3. ПОРЯДОК РАСЧЕТОВ И СУММА ДОГОВОРА</h6>
        <p>3.1. Цена Товара и дополнительных услуг определяется в момент заключения Основного Договора:</p>
        <p>3.1.1. в момент заключения Договора предоплаты Покупатель вносит предоплату на счет Продавца в размере
          {{ money }} тенге;</p>
        <p>3.1.2. оставшуюся сумму Покупатель оплачивает в момент заключения Основного Договора.</p>

        <h6>4. СРОК ДЕЙСТВИЯ ДОГОВОРА</h6>
        <p>4.1. Договор вступает в силу с момента его подписания.</p>
        <p>4.2. Датой окончания договора будет дата передачи Покупателю или лицам, его представляющим, Товара, соответствующего описанию, указанному в Приложениях Основного Договора. При оказании услуг, указанных в Договоре, Договор считается исполненным с момента выполнения этих услуг.</p>

        <h6>5. ОТВЕТСТВЕННОСТЬ СТОРОН</h6>
        <p>5.1. Право собственности на Товар переходит к Покупателю в момент 100% оплаты стоимости Товара.</p>
        <p>5.2. В случае отказа Покупателем от Товара, после его письменного обращения, Продавец, в течение 14 (четырнадцати) рабочих дней, возвращает сумму, оплаченную Покупателем за Товар, за вычетом фактически понесенных Продавцом расходов.</p>
        <p>5.3. Стороны освобождаются от ответственности за частичное или полное неисполнение обязательств по настоящему договору, если это неисполнение явилось следствием обстоятельств непреодолимой силы, возникших после заключения настоящего договора в результате событий чрезвычайного характера, которые сторона не могла предвидеть или предотвратить разумными мерами (форс-мажорные обстоятельства). К таким событиям относятся наводнения, пожар, землетрясения, взрыв, шторм, оседание почвы, эпидемия и иные явления природы, военные действия, технологические катастрофы. </p>

        <h6>6. РАЗРЕШЕНИЕ СПОРОВ</h6>
        <p>6.1. Все разногласия и споры, которые могут возникнуть между сторонами из настоящего договора и в связи с ним, будут по возможности решаться путем переговоров.</p>
        <p>6.2. В случае, когда возникшие споры путем переговоров не урегулированы, они подлежат разрешению в судах по месту нахождения Продавца.</p>
        <h6>7.	ФОРС-МАЖОРНЫЕ ОБСТОЯТЕЛЬСТВА</h6>
        <p>7.1 В случае наступления форс-мажорных обстоятельств пострадавшая Сторона обязана в кратчайшие сроки предупредить другую Сторону о невозможности исполнения своих обязательств по настоящему Договору.</p>
        <p>7.2. При этом ни одна Сторона не может требовать возмещения каких-либо убытков или потерь, связанных с невыполнением Договора.</p>

        <h6>8. ПРОЧИЕ УСЛОВИЯ ДОГОВОРА</h6>
        <p>8.1. Настоящий Договор, а также любые приложения к нему, заключается между двумя Сторонами в двух экземплярах, имеющих равную юридическую силу, и передаются по одному экземпляру каждой из сторон.</p>
        <p>8.2. Ни одна из сторон договора не вправе передавать свои права по Договору другому лицу без письменного согласия другой Стороны.</p>


        <h6>9. АДРЕСА И РЕКВИЗИТЫ СТОРОН.</h6>

        <table>
          <tr>
            <td>
              <h4>ПРОДАВЕЦ:</h4>
              ТОО «Test»
            </td>
            <td >
              <h4>ПОКУПАТЕЛЬ:</h4>
              наименование  ФИО {{fullName}}

            </td>
          </tr>
          <tr>
            <td>Юр. адрес: г. Алматы, ул. Дундича д. 245</td>
            <td>
              <div style="display: flex; flex-direction: column">
              <span>Регистрация: {{registration}}</span>
              <span>Место жительство: {{livingIn}} </span>
              <span>Телефон: {{phoneNumber}}</span>
            </div>
            </td>
          </tr>
          <tr>
            <td>Почтовый адрес:00000</td>
            <td>Почтовый адрес: {{email}}</td>
          </tr>
          <tr>
            <td>БИН: 1111111111</td>
            <td>ИИН {{iin}}</td>
          </tr>
          <tr>
            <td>
              <div style="display: flex; flex-direction: column">
              <span>АО «KaspiBank»</span>
              <span>p/c: 11111111111</span>
              <span>БИК: CASPKZKA</span>
              </div>
            </td>
            <td>
              <div style="display: flex; flex-direction: column">
                <span>Удост. личности №: {{udostakNumber}}</span>
                <span>Выдано когда: {{ udostakDate }}  . Кем:{{udostakByWho}}</span>
              </div>
            </td>
          </tr>
        </table>


      </div>
    </div>


  </div>
    </div>
    </div>


<!--inputs right logic-->

    <div class="right-logic">
      <label>Число:
      </label>
      <input type="number" placeholder="00" v-model="dayInput" @input="updateDay" />

      <label> Месяц:
      </label>
      <input type="text" placeholder="Введите данные" v-model="monthInput" />

      <label> День недели
      </label>
      <input type="text" placeholder="Введите данные" v-model="dayOfWeekInput"/>

      <label> Полное имя
      </label>
      <input type="text" placeholder="Введите данные" v-model="fullNameInput"/>

      <label> Номер удостоверения личности
      </label>
      <input type="number" placeholder="Введите данные" v-model="udostakNumberInput"/>

      <label> Дата выдачи удостоверения личности
      </label>
      <input type="text" placeholder="00.00.0000" v-model="udostakDateInput"/>

      <label> Кем выдано удостоверение личности
      </label>
      <input type="text" placeholder="Введите данные" v-model="udostakByWhoInput"/>

      <label> Место жительства
      </label>
      <input type="text" placeholder="Введите данные" v-model="livingInInput"/>

      <label> Дополнительные услуги
      </label>
      <input type="text" placeholder="Введите данные" v-model="dopUslugiInput"/>

      <label> Предоплата
      </label>
      <input type="number" placeholder="Введите данные" v-model="moneyInput"/>

      <label> Регистрация
      </label>
      <input type="text" placeholder="Введите данные" v-model="registrationInput"/>


      <label> Номер телефона
      </label>
      <input type="number" placeholder="87007770077" v-model="phoneNumberInput"/>

      <label> Почтовый адрес
      </label>
      <input type="email" placeholder="Введите данные" v-model="emailInput"/>

      <label> ИИН
      </label>
      <input type="number" placeholder="Введите данные" v-model="iinInput"/>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      isExpanded: false,
      showPaper: false,
      dayInput: '',
      monthInput: '',
      dayOfWeekInput: '' ,
      fullNameInput: '',
      livingInInput: '',
      udostakNumberInput: '',
      udostakDateInput: '',
      udostakByWhoInput: '',
      dopUslugiInput: '',
      moneyInput: '',
      registrationInput: '',
      phoneNumberInput: '',
      emailInput: '',
      iinInput: ''






    }
  },
  computed: {
    expandIcon() {
      return this.isExpanded ? 'expand_less' : 'expand_more';
    },
    day() {
      return this.dayInput;
    },
    month() {
      return this.monthInput;
    },
    dayOfWeek() {
      return this.dayOfWeekInput;
    },
    fullName() {
      return this.fullNameInput;
    },
    livingIn(){
      return this.livingInInput;
    },
    udostakNumber(){
      return this.udostakNumberInput;
    },
    udostakDate(){
      return this.udostakDateInput;
    },
    udostakByWho(){
      return this.udostakByWhoInput;
    },
    dopUslugi(){
      return this.dopUslugiInput;
    },
    money(){
      return this.moneyInput;
    },
    registration(){
      return this.registrationInput;
    },
    phoneNumber(){
      return this.phoneNumberInput;
    },
    email(){
      return this.emailInput;
    },
    iin(){
      return this.iinInput;
    }
  },
  methods: {
    showA4Page() {
      this.showPaper = !this.showPaper;
      this.isExpanded = !this.isExpanded;
    },
    updateDay() {
      this.dayInput = this.dayInput.slice(0, 2);
    },

  },
  name: 'A4Page'
}

</script>

