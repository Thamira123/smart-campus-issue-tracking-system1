<template>
  <q-page class="login-page">

    <!-- BACKGROUND DECORATION -->
    <div class="login-bg">
      <div class="bg-circle circle-1"></div>
      <div class="bg-circle circle-2"></div>
    </div>


    <div class="login-wrapper">

      <!-- LEFT PANEL — BRANDING -->
      <div class="login-left">

        <div class="left-content">

          <!-- BRAND -->
          <div class="brand" @click="goHome">

            <div class="brand-icon">
              <q-icon name="school" size="22px" />
            </div>

            <div class="brand-text">
              <div class="brand-name">CAMPUSCARE</div>
              <div class="brand-subtitle">SMART CAMPUS</div>
            </div>

          </div>


          <h1 class="left-title">
            Welcome
            <span>back.</span>
          </h1>

          <p class="left-description">
            Sign in to manage campus issues, track
            progress and help make your university
            a better place.
          </p>


          <!-- TRUST INDICATORS -->
          <div class="left-features">

            <div class="left-feature">
              <div class="feature-dot"></div>
              <span>Report &amp; track campus issues</span>
            </div>

            <div class="left-feature">
              <div class="feature-dot"></div>
              <span>Real-time status updates</span>
            </div>

            <div class="left-feature">
              <div class="feature-dot"></div>
              <span>Connected campus community</span>
            </div>

          </div>

        </div>

      </div>


      <!-- RIGHT PANEL — LOGIN FORM -->
      <div class="login-right">

        <div class="form-container">

          <!-- FORM HEADER -->
          <div class="form-header">

            <h2>Sign In</h2>

            <p>
              Enter your credentials to access
              your account
            </p>

          </div>


          <!-- FORM -->
          <form
            class="login-form"
            @submit.prevent="onSubmit"
          >

            <!-- EMAIL -->
            <div class="form-group">

              <label for="email">
                Email Address
              </label>

              <div class="input-wrapper">

                <q-icon
                  name="mail"
                  class="input-icon"
                />

                <input
                  id="email"
                  v-model="email"
                  type="email"
                  placeholder="you@campus.edu"
                  required
                />

              </div>

            </div>


            <!-- PASSWORD -->
            <div class="form-group">

              <div class="label-row">

                <label for="password">
                  Password
                </label>

                <a
                  href="#"
                  class="forgot-link"
                  @click.prevent="forgotPassword"
                >
                  Forgot password?
                </a>

              </div>

              <div class="input-wrapper">

                <q-icon
                  name="lock"
                  class="input-icon"
                />

                <input
                  id="password"
                  v-model="password"
                  :type="showPassword ? 'text' : 'password'"
                  placeholder="Enter your password"
                  required
                />

                <q-icon
                  :name="showPassword
                    ? 'visibility_off'
                    : 'visibility'"
                  class="toggle-icon"
                  @click="showPassword = !showPassword"
                />

              </div>

            </div>


            <!-- REMEMBER ME -->
            <div class="remember-row">

              <label class="checkbox-label">

                <input
                  v-model="rememberMe"
                  type="checkbox"
                />

                <span class="checkmark"></span>
                Remember me

              </label>

            </div>


            <!-- SUBMIT -->
            <q-btn
              unelevated
              no-caps
              type="submit"
              label="Sign In"
              icon-right="arrow_forward"
              class="submit-btn"
              :loading="loading"
            />

          </form>


          <!-- DIVIDER -->
          <div class="form-divider">

            <span>or</span>

          </div>


          <!-- BACK TO HOME -->
          <q-btn
            flat
            no-caps
            label="Back to Home"
            icon="arrow_back"
            class="home-btn"
            @click="goHome"
          />

        </div>

      </div>

    </div>

  </q-page>
</template>


<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()

const email = ref('')
const password = ref('')
const showPassword = ref(false)
const rememberMe = ref(false)
const loading = ref(false)

function onSubmit () {
  loading.value = true

  console.log('Login attempt:', {
    email: email.value,
    password: password.value,
    rememberMe: rememberMe.value
  })

  // Simulate login — replace with real auth later
  setTimeout(() => {
    loading.value = false
  }, 1500)
}

function forgotPassword () {
  console.log('Forgot password clicked')
}

function goHome () {
  router.push('/')
}
</script>


<style scoped>

/* =====================================================
   BASE
===================================================== */

.login-page {
  width: 100%;
  min-height: 100vh;

  position: relative;

  overflow: hidden;

  font-family:
    Inter,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;
}


/* BACKGROUND */

.login-bg {
  position: fixed;

  inset: 0;

  z-index: 0;

  background: #f8fafc;
}


.bg-circle {
  position: absolute;

  border-radius: 50%;
}


.circle-1 {
  width: 600px;
  height: 600px;

  top: -200px;
  left: -180px;

  background: rgba(37, 99, 235, 0.06);

  filter: blur(50px);
}


.circle-2 {
  width: 400px;
  height: 400px;

  bottom: -120px;
  right: -100px;

  background: rgba(37, 99, 235, 0.04);

  filter: blur(40px);
}


/* =====================================================
   LAYOUT
===================================================== */

.login-wrapper {
  position: relative;

  z-index: 1;

  width: 100%;
  min-height: 100vh;

  display: grid;

  grid-template-columns: 1fr 1fr;
}


/* =====================================================
   LEFT PANEL
===================================================== */

.login-left {
  display: flex;

  align-items: center;

  padding: 60px 60px 60px 80px;

  box-sizing: border-box;

  background:
    radial-gradient(
      circle at 30% 50%,
      rgba(37, 99, 235, 0.07),
      transparent 50%
    );
}


.left-content {
  max-width: 480px;
}


/* BRAND */

.brand {
  display: flex;

  align-items: center;

  gap: 11px;

  cursor: pointer;

  margin-bottom: 55px;
}


.brand-icon {
  width: 42px;
  height: 42px;

  flex-shrink: 0;

  border-radius: 12px;

  display: flex;

  align-items: center;

  justify-content: center;

  background: #0f4cdb;

  color: white;

  box-shadow:
    0 8px 20px rgba(15, 76, 219, 0.20);
}


.brand-name {
  font-size: 15px;

  font-weight: 800;

  letter-spacing: 0.8px;

  color: #10213d;
}


.brand-subtitle {
  margin-top: 2px;

  font-size: 8px;

  font-weight: 700;

  letter-spacing: 1.8px;

  color: #64748b;
}


/* LEFT CONTENT */

.left-title {
  margin: 0;

  font-size: clamp(46px, 4.5vw, 64px);

  line-height: 1;

  letter-spacing: -3px;

  font-weight: 850;

  color: #0b1830;
}


.left-title span {
  display: block;

  color: #1657d8;
}


.left-description {
  max-width: 400px;

  margin: 25px 0 40px;

  color: #64748b;

  font-size: 16px;

  line-height: 1.75;
}


/* LEFT FEATURES */

.left-features {
  display: flex;

  flex-direction: column;

  gap: 14px;
}


.left-feature {
  display: flex;

  align-items: center;

  gap: 11px;
}


.feature-dot {
  width: 7px;
  height: 7px;

  flex-shrink: 0;

  border-radius: 50%;

  background: #2563eb;

  box-shadow:
    0 0 0 4px rgba(37, 99, 235, 0.10);
}


.left-feature span {
  color: #475569;

  font-size: 13px;

  font-weight: 600;
}


/* =====================================================
   RIGHT PANEL
===================================================== */

.login-right {
  display: flex;

  align-items: center;

  justify-content: center;

  padding: 60px;

  box-sizing: border-box;
}


.form-container {
  width: 100%;
  max-width: 420px;

  padding: 40px;

  box-sizing: border-box;

  background: rgba(255, 255, 255, 0.98);

  border: 1px solid #e2e8f0;

  border-radius: 22px;

  box-shadow:
    0 30px 70px rgba(15, 23, 42, 0.10),
    0 8px 20px rgba(15, 23, 42, 0.03);
}


/* FORM HEADER */

.form-header {
  margin-bottom: 30px;
}


.form-header h2 {
  margin: 0;

  font-size: 26px;

  font-weight: 800;

  color: #0b1830;

  letter-spacing: -0.8px;
}


.form-header p {
  margin: 8px 0 0;

  color: #94a3b8;

  font-size: 13px;
}


/* FORM */

.login-form {
  display: flex;

  flex-direction: column;

  gap: 20px;
}


.form-group {
  display: flex;

  flex-direction: column;

  gap: 7px;
}


.form-group label {
  color: #334155;

  font-size: 12px;

  font-weight: 700;
}


.label-row {
  display: flex;

  justify-content: space-between;

  align-items: center;
}


.forgot-link {
  color: #2563eb;

  font-size: 11px;

  font-weight: 600;

  text-decoration: none;

  transition: 0.2s;
}


.forgot-link:hover {
  color: #1d4ed8;
}


/* INPUT */

.input-wrapper {
  position: relative;

  display: flex;

  align-items: center;
}


.input-icon {
  position: absolute;

  left: 14px;

  color: #94a3b8;

  font-size: 18px;

  pointer-events: none;
}


.toggle-icon {
  position: absolute;

  right: 14px;

  color: #94a3b8;

  font-size: 18px;

  cursor: pointer;

  transition: 0.2s;
}


.toggle-icon:hover {
  color: #64748b;
}


.input-wrapper input {
  width: 100%;

  height: 48px;

  padding: 0 44px;

  box-sizing: border-box;

  border: 1.5px solid #e2e8f0;

  border-radius: 12px;

  background: #f8fafc;

  color: #0f172a;

  font-size: 14px;

  font-family: inherit;

  outline: none;

  transition: 0.2s;
}


.input-wrapper input::placeholder {
  color: #94a3b8;
}


.input-wrapper input:focus {
  border-color: #2563eb;

  background: white;

  box-shadow:
    0 0 0 3px rgba(37, 99, 235, 0.08);
}


/* REMEMBER ME */

.remember-row {
  display: flex;

  align-items: center;
}


.checkbox-label {
  display: flex;

  align-items: center;

  gap: 8px;

  color: #64748b;

  font-size: 12px;

  font-weight: 600;

  cursor: pointer;

  user-select: none;
}


.checkbox-label input {
  display: none;
}


.checkmark {
  width: 16px;
  height: 16px;

  flex-shrink: 0;

  border: 1.5px solid #cbd5e1;

  border-radius: 4px;

  background: white;

  transition: 0.2s;

  position: relative;
}


.checkbox-label input:checked + .checkmark {
  background: #2563eb;

  border-color: #2563eb;
}


.checkbox-label input:checked + .checkmark::after {
  content: "";

  position: absolute;

  left: 4.5px;
  top: 1.5px;

  width: 4px;
  height: 8px;

  border: solid white;

  border-width: 0 2px 2px 0;

  transform: rotate(45deg);
}


/* SUBMIT */

.submit-btn {
  width: 100%;

  min-height: 48px;

  border-radius: 12px;

  background: #0f4cdb;

  color: white;

  font-size: 14px;

  font-weight: 700;

  box-shadow:
    0 10px 25px rgba(15, 76, 219, 0.22);

  margin-top: 4px;
}


/* DIVIDER */

.form-divider {
  display: flex;

  align-items: center;

  margin: 22px 0;
}


.form-divider::before,
.form-divider::after {
  content: "";

  flex: 1;

  height: 1px;

  background: #e2e8f0;
}


.form-divider span {
  padding: 0 14px;

  color: #94a3b8;

  font-size: 11px;

  font-weight: 600;
}


/* HOME BUTTON */

.home-btn {
  width: 100%;

  min-height: 44px;

  border-radius: 10px;

  color: #64748b;

  font-weight: 600;
}


.home-btn:hover {
  color: #334155;

  background: #f1f5f9;
}


/* =====================================================
   RESPONSIVE
===================================================== */

@media (max-width: 1000px) {

  .login-wrapper {
    grid-template-columns: 1fr;
  }

  .login-left {
    display: none;
  }

  .login-right {
    padding: 40px 20px;
  }

}


@media (max-width: 500px) {

  .form-container {
    padding: 28px 22px;
  }

  .form-header h2 {
    font-size: 22px;
  }

}

</style>
