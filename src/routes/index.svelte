<script>
  import PageTitle from "../components/PageTitle.svelte";
  import Content from "../components/layouts/Content.svelte";
  import Button from "../components/atoms/Button.svelte";
  import {
    Tabs,
    TabList,
    TabPanel,
    Tab
  } from "../components/molecules/tabs.js";
</script>



<svelte:head>
  <title>TODH wellcome</title>
</svelte:head>

<PageTitle>
  <h1 slot="pagetitle">👋 hola!</h1>
  <h2 slot="subtitle">Esto esto va de arte, diseño front-end y mística</h2>
</PageTitle>

<Content>
  <div class="col-desk-9 col-tab-10 col-mob-4">
    <Tabs>
      <TabList>
        <Tab>Matriz TODH</Tab>
        <Tab>Obra gráfica</Tab>
        <Tab>Prototipado</Tab>
      </TabList>

      <TabPanel>
        <div class="grid-0">
          <div class="col-desk-6">
            <p>
              Proyecto interdisciplinar con el que trato de evanglizar a todo
              aquel incauto que me pregunta.
            </p>
            <Button text="Más info" href="./todh" />
          </div>
          <div class="col-desk-6">
            <img src="img/grafico-1.svg" alt="" />
          </div>
        </div>
      </TabPanel>

      <TabPanel>
        <div class="grid-0">
          <div class="col-desk-6">
            <p>
              Impresiones 3D a partir de matrices generadas por ordenador. Luego
              las trabajo con resina epoxi, cera, arena, etc...
            </p>
            <Button text="Más info" href="./artwork" />
          </div>
          <div class="col-desk-6">
            <img src="img/img3.jpg" alt="" />
          </div>
        </div>

      </TabPanel>

      <TabPanel>
        <p>
          Pasión por el diseño y prototipado UI en el front-end. Avido consumidor de servicios API y fiel aférrimo de las bases de la web: Html, Css/Sass,
          Svelte/Sapper y Git
        </p>

      </TabPanel>

    </Tabs>
  </div>
</Content>
