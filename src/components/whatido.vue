<template>
  <div class="whatido">
    <div class="container">
      <div class="text-h4 text-center text-weight-bolder q-pb-xl">What I Do</div>
      <div class="row justify-center q-col-gutter-lg">

        <!-- Web Development Section -->
        <div class="col-12 col-sm-8 col-md-6">
          <q-card class="what-i-do text-center shadow-9 hover-effect">
            <q-card-section>
              <q-avatar size="70px" rounded class="q-mr-sm">
                <img src="~/assets/website3.png" alt="Web Development Icon" />
              </q-avatar>
              <div class="text-h5 text-weight-bold q-mt-md">Web Development</div>
              <p class="q-mt-md text-left text-h6">
                Crafting dynamic, responsive, and secure websites tailored to your needs. My expertise includes integrating:
                <ul class="text-left q-mt-lg">
                  <li>Payment Gateways</li>
                  <li>Single Sign-On (SSO) for seamless authentication</li>
                </ul>
              </p>
            </q-card-section>
          </q-card>
        </div>

        <!-- Mobile Development Section -->
        <div class="col-12 col-sm-8 col-md-6">
          <q-card class="what-i-do text-center shadow-9 hover-effect">
            <q-card-section>
              <q-avatar size="70px" rounded class="q-mr-sm">
                <img src="~/assets/app.png" alt="Mobile Development Icon" style="object-fit:contain"/>
              </q-avatar>
              <div class="text-h5 text-weight-bold q-mt-md">Mobile Development</div>
              <p class="q-mt-md text-left text-h6">
                Building robust backend solutions for mobile applications. I ensure:
                <ul class="text-left q-mt-lg">
                  <li>Secure data handling with optimized APIs</li>
                  <li>Integration with third-party tools (e.g., push notifications, in-app purchases)</li>
                  <li>Scalable and efficient backend architecture</li>
                </ul>
              </p>
            </q-card-section>
          </q-card>
        </div>

        <!-- API Development Section -->
        <div class="col-12">
          <q-card class="what-i-do text-center shadow-9 hover-effect">
            <q-card-section>
              <q-avatar size="70px" rounded class="q-mr-sm">
                <img src="~/assets/app.png" alt="API Development Icon" style="object-fit:contain"/>
              </q-avatar>
              <div class="text-h5 text-weight-bold q-mt-md">API Development</div>
              <p class="q-mt-md text-left text-h6">
                I design and implement APIs tailored to your business needs. <br>
                Features include:
                <ul class="text-left q-mt-lg">
                  <li>Optimized performance for high-traffic applications</li>
                  <li>Integration with microservices and cloud platforms</li>
                  <li>Advanced data security and encryption protocols</li>
                </ul>
              </p>
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </div>
</template>
