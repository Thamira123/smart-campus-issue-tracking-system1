<template>
  <q-page class="home-page">

    <!-- ================= NAVBAR ================= -->
    <header class="navbar">
      <div class="nav-container">

        <!-- LOGO -->
        <div class="brand" @click="scrollToTop">
          <div class="brand-icon">
            <q-icon name="school" size="22px" />
          </div>

          <div class="brand-text">
            <div class="brand-name">CAMPUSCARE</div>
            <div class="brand-subtitle">SMART CAMPUS</div>
          </div>
        </div>

        <!-- NAVIGATION -->
        <nav class="desktop-nav">
          <a href="#home" class="nav-link active">Home</a>
          <a href="#how-it-works" class="nav-link">How It Works</a>
          <a href="#features" class="nav-link">Features</a>
          <a href="#about" class="nav-link">About</a>
        </nav>

        <!-- NAV ACTIONS -->
        <div class="nav-actions">

          <q-btn
            flat
            no-caps
            label="Login"
            class="login-btn"
            @click="handleLogin"
          />

          <q-btn
            unelevated
            no-caps
            label="Report Issue"
            icon-right="arrow_forward"
            class="nav-report-btn"
            @click="reportIssue"
          />

        </div>

      </div>
    </header>


    <!-- ================= HERO ================= -->
    <section id="home" class="hero-section">

      <div class="hero-container">

        <!-- HERO LEFT -->
        <div class="hero-content">

          <div class="hero-badge">
            <span class="badge-dot"></span>
            Smart Campus Issue Management
          </div>

          <h1 class="hero-title">
            Make your campus
            <span>better.</span>
          </h1>

          <p class="hero-description">
            Report campus issues, track their progress, and stay
            connected with the people working to make your
            university a better place.
          </p>

          <div class="hero-buttons">

            <q-btn
              unelevated
              no-caps
              label="Report an Issue"
              icon="add_circle_outline"
              class="primary-btn"
              @click="reportIssue"
            />

            <q-btn
              flat
              no-caps
              label="Track an Issue"
              icon="search"
              class="secondary-btn"
              @click="trackIssue"
            />

          </div>

          <!-- TRUST -->
          <div class="hero-trust">

            <div class="trust-avatars">

              <div class="avatar avatar-1">S</div>
              <div class="avatar avatar-2">A</div>
              <div class="avatar avatar-3">K</div>

              <div class="avatar avatar-4">
                <q-icon name="add" size="15px" />
              </div>

            </div>

            <div class="trust-text">
              <strong>Built for campus communities</strong>
              <span>Students • Staff • Administration</span>
            </div>

          </div>

        </div>


        <!-- HERO RIGHT -->
        <div class="hero-visual">

          <div class="visual-glow"></div>

          <!-- DASHBOARD CARD -->
          <div class="dashboard-card">

            <!-- HEADER -->
            <div class="dashboard-header">

              <div>
                <span class="small-label">
                  CAMPUS OVERVIEW
                </span>

                <h3>
                  Issue Management
                </h3>
              </div>

              <div class="live-indicator">
                <span></span>
                Live
              </div>

            </div>


            <!-- MINI STATS -->
            <div class="mini-stats">

              <div class="mini-stat">

                <div class="mini-icon blue">
                  <q-icon name="assignment" />
                </div>

                <div>
                  <strong>128</strong>
                  <span>Total Issues</span>
                </div>

              </div>


              <div class="mini-stat">

                <div class="mini-icon orange">
                  <q-icon name="pending_actions" />
                </div>

                <div>
                  <strong>24</strong>
                  <span>Pending</span>
                </div>

              </div>

            </div>


            <!-- PROGRESS -->
            <div class="progress-section">

              <div class="progress-top">
                <span>Resolution Progress</span>
                <strong>78%</strong>
              </div>

              <div class="progress-bar">
                <div class="progress-value"></div>
              </div>

            </div>


            <!-- ISSUE LIST -->
            <div class="issue-list">

              <!-- ISSUE 01 -->
              <div class="issue-item">

                <div class="issue-icon maintenance">
                  <q-icon name="build" />
                </div>

                <div class="issue-info">

                  <strong>
                    Laboratory Equipment
                  </strong>

                  <span>
                    Engineering Faculty
                  </span>

                </div>

                <div class="status resolved">
                  Resolved
                </div>

              </div>


              <!-- ISSUE 02 -->
              <div class="issue-item">

                <div class="issue-icon it">
                  <q-icon name="wifi" />
                </div>

                <div class="issue-info">

                  <strong>
                    Wi-Fi Connectivity
                  </strong>

                  <span>
                    Main Library
                  </span>

                </div>

                <div class="status progress">
                  In Progress
                </div>

              </div>


              <!-- ISSUE 03 -->
              <div class="issue-item">

                <div class="issue-icon facility">
                  <q-icon name="lightbulb" />
                </div>

                <div class="issue-info">

                  <strong>
                    Classroom Lighting
                  </strong>

                  <span>
                    Science Faculty
                  </span>

                </div>

                <div class="status pending">
                  Pending
                </div>

              </div>

            </div>

          </div>

        </div>

      </div>


      <!-- HERO BOTTOM FEATURES -->
      <div class="hero-bottom">

        <div class="bottom-item">

          <div class="bottom-icon">
            <q-icon name="verified_user" />
          </div>

          <div>
            <strong>Transparent</strong>
            <span>Track every report</span>
          </div>

        </div>


        <div class="bottom-item">

          <div class="bottom-icon">
            <q-icon name="bolt" />
          </div>

          <div>
            <strong>Efficient</strong>
            <span>Faster issue resolution</span>
          </div>

        </div>


        <div class="bottom-item">

          <div class="bottom-icon">
            <q-icon name="groups" />
          </div>

          <div>
            <strong>Connected</strong>
            <span>One campus community</span>
          </div>

        </div>

      </div>

    </section>


    <!-- ================= HOW IT WORKS ================= -->
    <section
      id="how-it-works"
      class="section how-section"
    >

      <div class="section-heading">

        <div class="section-tag">
          SIMPLE PROCESS
        </div>

        <h2>
          From problem to solution.
        </h2>

        <p>
          A simple and transparent way to report campus
          problems and keep track of what happens next.
        </p>

      </div>


      <div class="steps-container">

        <!-- STEP 01 -->
        <div class="step-card">

          <div class="step-number">
            01
          </div>

          <div class="step-icon">
            <q-icon name="edit_note" />
          </div>

          <h3>
            Report
          </h3>

          <p>
            Submit an issue with its location, category,
            description and supporting details.
          </p>

          <span class="step-link">
            Easy reporting
            <q-icon name="arrow_forward" />
          </span>

        </div>


        <div class="step-line"></div>


        <!-- STEP 02 -->
        <div class="step-card">

          <div class="step-number">
            02
          </div>

          <div class="step-icon">
            <q-icon name="visibility" />
          </div>

          <h3>
            Track
          </h3>

          <p>
            Follow your issue from submission through
            review, assignment and resolution.
          </p>

          <span class="step-link">
            Real-time updates
            <q-icon name="arrow_forward" />
          </span>

        </div>


        <div class="step-line"></div>


        <!-- STEP 03 -->
        <div class="step-card">

          <div class="step-number">
            03
          </div>

          <div class="step-icon">
            <q-icon name="task_alt" />
          </div>

          <h3>
            Resolve
          </h3>

          <p>
            Campus teams take action and keep everyone
            informed until the issue is resolved.
          </p>

          <span class="step-link">
            Better campus
            <q-icon name="check" />
          </span>

        </div>

      </div>

    </section>


    <!-- ================= FEATURES ================= -->
    <section
      id="features"
      class="section features-section"
    >

      <div class="section-heading">

        <div class="section-tag">
          ONE PLATFORM
        </div>

        <h2>
          Everything your campus needs.
        </h2>

        <p>
          Designed to connect students, staff and administrators
          through one simple issue management platform.
        </p>

      </div>


      <div class="feature-grid">

        <!-- FEATURE 01 -->
        <div class="feature-card">

          <div class="feature-icon blue-bg">
            <q-icon name="report_problem" />
          </div>

          <h3>
            Smart Issue Reporting
          </h3>

          <p>
            Report maintenance, IT, facility and other
            campus problems from one place.
          </p>

          <span class="feature-arrow">
            <q-icon name="arrow_forward" />
          </span>

        </div>


        <!-- FEATURE 02 -->
        <div class="feature-card">

          <div class="feature-icon purple-bg">
            <q-icon name="location_on" />
          </div>

          <h3>
            Location Based
          </h3>

          <p>
            Clearly identify where an issue is located
            so the right team can respond faster.
          </p>

          <span class="feature-arrow">
            <q-icon name="arrow_forward" />
          </span>

        </div>


        <!-- FEATURE 03 -->
        <div class="feature-card">

          <div class="feature-icon green-bg">
            <q-icon name="timeline" />
          </div>

          <h3>
            Live Tracking
          </h3>

          <p>
            See the current status of your report and
            understand what happens at every stage.
          </p>

          <span class="feature-arrow">
            <q-icon name="arrow_forward" />
          </span>

        </div>


        <!-- FEATURE 04 -->
        <div class="feature-card">

          <div class="feature-icon orange-bg">
            <q-icon name="notifications_active" />
          </div>

          <h3>
            Instant Updates
          </h3>

          <p>
            Stay informed when your issue is reviewed,
            assigned, updated or resolved.
          </p>

          <span class="feature-arrow">
            <q-icon name="arrow_forward" />
          </span>

        </div>

      </div>

    </section>


    <!-- ================= CTA ================= -->
    <section
      id="about"
      class="cta-section"
    >

      <div class="cta-container">

        <div class="cta-content">

          <div class="cta-icon">
            <q-icon name="school" />
          </div>

          <div>

            <span class="cta-label">
              SMART CAMPUS INITIATIVE
            </span>

            <h2>
              Your campus.
              <span>Your voice.</span>
            </h2>

            <p>
              Help create a cleaner, safer and more connected
              university by reporting issues when you see them.
            </p>

          </div>

        </div>


        <q-btn
          unelevated
          no-caps
          label="Report an Issue"
          icon-right="arrow_forward"
          class="cta-btn"
          @click="reportIssue"
        />

      </div>

    </section>


    <!-- ================= FOOTER ================= -->
    <footer class="footer">

      <div class="footer-container">

        <!-- FOOTER BRAND -->
        <div class="footer-brand">

          <div class="brand">

            <div class="brand-icon">
              <q-icon
                name="school"
                size="20px"
              />
            </div>

            <div class="brand-text">

              <div class="brand-name">
                CAMPUSCARE
              </div>

              <div class="brand-subtitle">
                SMART CAMPUS
              </div>

            </div>

          </div>

          <p>
            A smarter way to build a better campus.
          </p>

        </div>


        <!-- FOOTER LINKS -->
        <div class="footer-links">

          <div class="footer-column">

            <h4>
              Platform
            </h4>

            <a href="#features">
              Features
            </a>

            <a href="#how-it-works">
              How It Works
            </a>

            <a href="#about">
              About
            </a>

          </div>


          <div class="footer-column">

            <h4>
              Support
            </h4>

            <a href="#">
              Help Center
            </a>

            <a href="#">
              Contact Us
            </a>

            <a href="#">
              Privacy
            </a>

          </div>


          <div class="footer-column">

            <h4>
              Campus
            </h4>

            <a href="#">
              Students
            </a>

            <a href="#">
              Staff
            </a>

            <a href="#">
              Administration
            </a>

          </div>

        </div>

      </div>


      <!-- FOOTER BOTTOM -->
      <div class="footer-bottom">

        <span>
          © 2026 CampusCare.
          Smart Campus Issue Tracking System.
        </span>

        <span>
          Built for a better campus.
        </span>

      </div>

    </footer>

  </q-page>
</template>


<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

function scrollToTop () {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  })
}

function reportIssue () {
  console.log('Report Issue clicked')

  // Later:
  // router.push('/report-issue')
}

function trackIssue () {
  console.log('Track Issue clicked')

  // Later:
  // router.push('/track-issue')
}

function handleLogin () {
  router.push('/login')
}

</script>


<style scoped>

/* =====================================================
   BASE
===================================================== */

.home-page {
  width: 100%;
  min-height: 100vh;

  background: #f8fafc;

  color: #0f172a;

  font-family:
    Inter,
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;

  overflow-x: hidden;
}


/* =====================================================
   NAVBAR
===================================================== */

.navbar {
  position: sticky;

  top: 0;

  z-index: 1000;

  height: 76px;

  background: rgba(255, 255, 255, 0.96);

  backdrop-filter: blur(18px);

  border-bottom: 1px solid #e8edf3;
}


.nav-container {
  width: 100%;
  max-width: 1240px;

  height: 100%;

  margin: auto;

  padding: 0 28px;

  box-sizing: border-box;

  display: flex;

  align-items: center;

  justify-content: space-between;
}


/* BRAND */

.brand {
  display: flex;

  align-items: center;

  gap: 11px;

  cursor: pointer;
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


/* NAV */

.desktop-nav {
  display: flex;

  align-items: center;

  gap: 34px;
}


.nav-link {
  position: relative;

  color: #64748b;

  text-decoration: none;

  font-size: 14px;

  font-weight: 600;

  transition: 0.25s;
}


.nav-link:hover,
.nav-link.active {
  color: #0f4cdb;
}


.nav-link.active::after {
  content: "";

  position: absolute;

  left: 0;
  right: 0;

  bottom: -10px;

  height: 2px;

  background: #0f4cdb;

  border-radius: 10px;
}


/* ACTIONS */

.nav-actions {
  display: flex;

  align-items: center;

  gap: 8px;
}


.login-btn {
  color: #334155;

  font-weight: 600;
}


.nav-report-btn {
  min-height: 42px;

  padding: 0 18px;

  border-radius: 10px;

  background: #0f4cdb;

  color: white;

  font-weight: 700;

  box-shadow:
    0 7px 18px rgba(15, 76, 219, 0.18);
}


/* =====================================================
   HERO
===================================================== */

.hero-section {
  position: relative;

  background:
    radial-gradient(
      circle at 80% 25%,
      rgba(37, 99, 235, 0.09),
      transparent 32%
    ),
    #f8fafc;
}


.hero-container {
  width: 100%;
  max-width: 1240px;

  min-height: 610px;

  margin: auto;

  padding: 90px 28px 55px;

  box-sizing: border-box;

  display: grid;

  grid-template-columns: 1fr 0.92fr;

  align-items: center;

  gap: 70px;
}


/* HERO LEFT */

.hero-content {
  max-width: 610px;
}


.hero-badge {
  display: inline-flex;

  align-items: center;

  gap: 9px;

  padding: 8px 13px;

  border-radius: 30px;

  background: #eaf1ff;

  color: #2358b8;

  font-size: 12px;

  font-weight: 700;

  letter-spacing: 0.3px;

  margin-bottom: 22px;
}


.badge-dot {
  width: 7px;
  height: 7px;

  border-radius: 50%;

  background: #2563eb;

  box-shadow:
    0 0 0 4px rgba(37, 99, 235, 0.10);
}


.hero-title {
  margin: 0;

  font-size: clamp(50px, 5vw, 76px);

  line-height: 0.98;

  letter-spacing: -3.5px;

  font-weight: 850;

  color: #0b1830;
}


.hero-title span {
  display: block;

  color: #1657d8;
}


.hero-description {
  max-width: 540px;

  margin: 28px 0 30px;

  color: #64748b;

  font-size: 17px;

  line-height: 1.75;
}


/* BUTTONS */

.hero-buttons {
  display: flex;

  align-items: center;

  gap: 12px;
}


.primary-btn {
  min-height: 52px;

  padding: 0 22px;

  border-radius: 11px;

  background: #0f4cdb;

  color: white;

  font-size: 14px;

  font-weight: 700;

  box-shadow:
    0 10px 25px rgba(15, 76, 219, 0.22);
}


.secondary-btn {
  min-height: 52px;

  padding: 0 20px;

  border-radius: 11px;

  color: #1e3a5f;

  font-weight: 700;
}


/* TRUST */

.hero-trust {
  margin-top: 34px;

  display: flex;

  align-items: center;

  gap: 13px;
}


.trust-avatars {
  display: flex;
}


.avatar {
  width: 30px;
  height: 30px;

  border-radius: 50%;

  margin-left: -7px;

  border: 2px solid #f8fafc;

  display: flex;

  align-items: center;

  justify-content: center;

  font-size: 10px;

  font-weight: 800;

  background: #dbeafe;

  color: #1d4ed8;
}


.avatar:first-child {
  margin-left: 0;
}


.avatar-2 {
  background: #e0e7ff;

  color: #4338ca;
}


.avatar-3 {
  background: #dcfce7;

  color: #15803d;
}


.avatar-4 {
  background: #0f4cdb;

  color: white;
}


.trust-text {
  display: flex;

  flex-direction: column;

  gap: 2px;
}


.trust-text strong {
  font-size: 12px;

  color: #334155;
}


.trust-text span {
  font-size: 11px;

  color: #94a3b8;
}


/* =====================================================
   HERO VISUAL
===================================================== */

.hero-visual {
  position: relative;

  min-height: 460px;

  display: flex;

  align-items: center;

  justify-content: center;
}


.visual-glow {
  position: absolute;

  width: 370px;
  height: 370px;

  border-radius: 50%;

  background: rgba(37, 99, 235, 0.09);

  filter: blur(30px);
}


/* DASHBOARD */

.dashboard-card {
  position: relative;

  width: min(480px, 100%);

  padding: 25px;

  box-sizing: border-box;

  border-radius: 20px;

  background: rgba(255, 255, 255, 0.98);

  border: 1px solid #e2e8f0;

  box-shadow:
    0 30px 70px rgba(15, 23, 42, 0.12),
    0 8px 20px rgba(15, 23, 42, 0.04);

  z-index: 2;
}


.dashboard-header {
  display: flex;

  justify-content: space-between;

  align-items: flex-start;

  margin-bottom: 22px;
}


.small-label {
  color: #94a3b8;

  font-size: 9px;

  font-weight: 800;

  letter-spacing: 1.5px;
}


.dashboard-header h3 {
  margin: 5px 0 0;

  font-size: 20px;

  color: #12233f;
}


.live-indicator {
  display: flex;

  align-items: center;

  gap: 6px;

  padding: 6px 9px;

  border-radius: 20px;

  background: #ecfdf5;

  color: #15803d;

  font-size: 10px;

  font-weight: 700;
}


.live-indicator span {
  width: 6px;
  height: 6px;

  border-radius: 50%;

  background: #22c55e;
}


/* MINI STATS */

.mini-stats {
  display: grid;

  grid-template-columns: 1fr 1fr;

  gap: 12px;

  margin-bottom: 22px;
}


.mini-stat {
  padding: 15px;

  display: flex;

  align-items: center;

  gap: 11px;

  background: #f8fafc;

  border: 1px solid #edf2f7;

  border-radius: 12px;
}


.mini-icon {
  width: 38px;
  height: 38px;

  border-radius: 10px;

  display: flex;

  align-items: center;

  justify-content: center;
}


.mini-icon.blue {
  background: #eaf1ff;

  color: #2563eb;
}


.mini-icon.orange {
  background: #fff7ed;

  color: #ea580c;
}


.mini-stat strong {
  display: block;

  font-size: 19px;

  color: #142541;
}


.mini-stat span {
  display: block;

  margin-top: 1px;

  font-size: 10px;

  color: #94a3b8;
}


/* PROGRESS */

.progress-section {
  margin-bottom: 22px;
}


.progress-top {
  display: flex;

  justify-content: space-between;

  margin-bottom: 8px;

  font-size: 11px;

  color: #64748b;
}


.progress-top strong {
  color: #2563eb;
}


.progress-bar {
  height: 7px;

  border-radius: 10px;

  background: #e9eef5;

  overflow: hidden;
}


.progress-value {
  width: 78%;

  height: 100%;

  border-radius: inherit;

  background: #2563eb;
}


/* ISSUE LIST */

.issue-list {
  display: flex;

  flex-direction: column;

  gap: 9px;
}


.issue-item {
  display: flex;

  align-items: center;

  gap: 10px;

  padding: 11px 10px;

  border-radius: 11px;

  transition: 0.2s;
}


.issue-item:hover {
  background: #f8fafc;
}


.issue-icon {
  width: 34px;
  height: 34px;

  flex-shrink: 0;

  border-radius: 9px;

  display: flex;

  align-items: center;

  justify-content: center;
}


.issue-icon.maintenance {
  background: #eef2ff;

  color: #4f46e5;
}


.issue-icon.it {
  background: #e0f2fe;

  color: #0284c7;
}


.issue-icon.facility {
  background: #fef3c7;

  color: #d97706;
}


.issue-info {
  flex: 1;

  min-width: 0;
}


.issue-info strong {
  display: block;

  color: #334155;

  font-size: 11px;
}


.issue-info span {
  display: block;

  margin-top: 2px;

  color: #94a3b8;

  font-size: 9px;
}


/* STATUS */

.status {
  flex-shrink: 0;

  padding: 5px 8px;

  border-radius: 20px;

  font-size: 8px;

  font-weight: 800;
}


.status.resolved {
  color: #15803d;

  background: #dcfce7;
}


.status.progress {
  color: #1d4ed8;

  background: #dbeafe;
}


.status.pending {
  color: #b45309;

  background: #fef3c7;
}


/* =====================================================
   HERO BOTTOM
===================================================== */

.hero-bottom {
  width: 100%;
  max-width: 1184px;

  margin: auto;

  padding: 25px 0;

  border-top: 1px solid #e2e8f0;

  display: grid;

  grid-template-columns: repeat(3, 1fr);

  gap: 30px;
}


.bottom-item {
  display: flex;

  align-items: center;

  gap: 12px;
}


.bottom-icon {
  width: 38px;
  height: 38px;

  flex-shrink: 0;

  display: flex;

  align-items: center;

  justify-content: center;

  border-radius: 10px;

  background: white;

  color: #2563eb;
}


.bottom-item strong {
  display: block;

  font-size: 12px;

  color: #334155;
}


.bottom-item span {
  display: block;

  margin-top: 3px;

  font-size: 10px;

  color: #94a3b8;
}


/* =====================================================
   SECTIONS
===================================================== */

.section {
  padding: 105px 28px;

  box-sizing: border-box;
}


.section-heading {
  max-width: 670px;

  margin: 0 auto 60px;

  text-align: center;
}


.section-tag {
  color: #2563eb;

  font-size: 10px;

  font-weight: 800;

  letter-spacing: 1.8px;

  margin-bottom: 13px;
}


.section-heading h2 {
  margin: 0;

  color: #10213d;

  font-size: clamp(34px, 4vw, 46px);

  line-height: 1.1;

  letter-spacing: -1.8px;
}


.section-heading p {
  margin: 18px auto 0;

  max-width: 580px;

  color: #64748b;

  font-size: 15px;

  line-height: 1.7;
}


/* =====================================================
   HOW IT WORKS
===================================================== */

.how-section {
  background: white;
}


.steps-container {
  max-width: 1120px;

  margin: auto;

  display: grid;

  grid-template-columns:
    1fr
    auto
    1fr
    auto
    1fr;

  align-items: center;
}


.step-card {
  position: relative;

  padding: 30px;

  min-height: 260px;

  box-sizing: border-box;

  border: 1px solid #e6ebf2;

  border-radius: 17px;

  background: #ffffff;

  transition: 0.3s;
}


.step-card:hover {
  transform: translateY(-5px);

  border-color: #cbdaf8;

  box-shadow:
    0 18px 40px rgba(15, 23, 42, 0.07);
}


.step-number {
  position: absolute;

  right: 22px;

  top: 20px;

  color: #dce7f8;

  font-size: 30px;

  font-weight: 900;
}


.step-icon {
  width: 50px;
  height: 50px;

  margin-bottom: 22px;

  border-radius: 13px;

  display: flex;

  align-items: center;

  justify-content: center;

  background: #eaf1ff;

  color: #2563eb;

  font-size: 23px;
}


.step-card h3 {
  margin: 0 0 10px;

  color: #172b4d;

  font-size: 20px;
}


.step-card p {
  margin: 0;

  color: #64748b;

  font-size: 13px;

  line-height: 1.7;
}


.step-link {
  display: flex;

  align-items: center;

  gap: 5px;

  margin-top: 18px;

  color: #2563eb;

  font-size: 11px;

  font-weight: 700;
}


.step-line {
  width: 45px;

  height: 1px;

  background: #cbd5e1;
}


/* =====================================================
   FEATURES
===================================================== */

.features-section {
  background: #f8fafc;
}


.feature-grid {
  max-width: 1120px;

  margin: auto;

  display: grid;

  grid-template-columns: repeat(4, 1fr);

  gap: 15px;
}


.feature-card {
  position: relative;

  min-height: 270px;

  padding: 27px;

  box-sizing: border-box;

  background: white;

  border: 1px solid #e5eaf1;

  border-radius: 17px;

  transition: 0.3s;
}


.feature-card:hover {
  transform: translateY(-5px);

  box-shadow:
    0 18px 45px rgba(15, 23, 42, 0.07);
}


.feature-icon {
  width: 48px;
  height: 48px;

  border-radius: 13px;

  display: flex;

  align-items: center;

  justify-content: center;

  font-size: 22px;

  margin-bottom: 22px;
}


.blue-bg {
  background: #eaf1ff;

  color: #2563eb;
}


.purple-bg {
  background: #f1edff;

  color: #7c3aed;
}


.green-bg {
  background: #e8f8ef;

  color: #16a34a;
}


.orange-bg {
  background: #fff1e8;

  color: #ea580c;
}


.feature-card h3 {
  margin: 0 0 10px;

  color: #172b4d;

  font-size: 17px;
}


.feature-card p {
  margin: 0;

  color: #64748b;

  font-size: 12px;

  line-height: 1.75;
}


.feature-arrow {
  position: absolute;

  left: 27px;

  bottom: 24px;

  color: #2563eb;

  font-size: 16px;
}


/* =====================================================
   CTA
===================================================== */

.cta-section {
  padding: 80px 28px;

  box-sizing: border-box;

  background: white;
}


.cta-container {
  max-width: 1120px;

  margin: auto;

  padding: 45px 50px;

  box-sizing: border-box;

  border-radius: 22px;

  background: #0f2343;

  display: flex;

  align-items: center;

  justify-content: space-between;

  gap: 30px;

  overflow: hidden;

  position: relative;
}


.cta-container::after {
  content: "";

  position: absolute;

  width: 300px;
  height: 300px;

  right: -100px;
  top: -140px;

  border-radius: 50%;

  background: rgba(37, 99, 235, 0.20);
}


.cta-content {
  display: flex;

  align-items: center;

  gap: 20px;

  position: relative;

  z-index: 2;
}


.cta-icon {
  width: 58px;
  height: 58px;

  flex-shrink: 0;

  border-radius: 15px;

  display: flex;

  align-items: center;

  justify-content: center;

  background: rgba(255, 255, 255, 0.10);

  color: #93c5fd;

  font-size: 25px;
}


.cta-label {
  color: #93c5fd;

  font-size: 9px;

  font-weight: 800;

  letter-spacing: 1.5px;
}


.cta-content h2 {
  margin: 5px 0 7px;

  color: white;

  font-size: 31px;

  letter-spacing: -1px;
}


.cta-content h2 span {
  color: #72a8ff;
}


.cta-content p {
  max-width: 560px;

  margin: 0;

  color: #a8b7ce;

  font-size: 12px;

  line-height: 1.6;
}


.cta-btn {
  position: relative;

  z-index: 3;

  min-height: 48px;

  padding: 0 20px;

  border-radius: 10px;

  background: white;

  color: #123b7b;

  font-weight: 800;

  white-space: nowrap;
}


/* =====================================================
   FOOTER
===================================================== */

.footer {
  background: #09172d;

  color: white;

  padding: 60px 28px 25px;

  box-sizing: border-box;
}


.footer-container {
  max-width: 1120px;

  margin: auto;

  display: grid;

  grid-template-columns: 1.4fr 1fr;

  gap: 80px;
}


.footer-brand p {
  max-width: 250px;

  margin-top: 18px;

  color: #8293ad;

  font-size: 12px;

  line-height: 1.6;
}


.footer-links {
  display: grid;

  grid-template-columns: repeat(3, 1fr);

  gap: 30px;
}


.footer-column {
  display: flex;

  flex-direction: column;

  gap: 10px;
}


.footer-column h4 {
  margin: 0 0 8px;

  font-size: 11px;

  letter-spacing: 0.5px;

  color: white;
}


.footer-column a {
  color: #8293ad;

  text-decoration: none;

  font-size: 11px;

  transition: 0.2s;
}


.footer-column a:hover {
  color: white;
}


.footer-bottom {
  max-width: 1120px;

  margin: 50px auto 0;

  padding-top: 20px;

  border-top: 1px solid rgba(255, 255, 255, 0.08);

  display: flex;

  justify-content: space-between;

  color: #64748b;

  font-size: 10px;
}


/* =====================================================
   RESPONSIVE
===================================================== */

@media (max-width: 1100px) {

  .desktop-nav {
    gap: 20px;
  }

  .hero-container {
    gap: 40px;
  }

  .feature-grid {
    grid-template-columns: repeat(2, 1fr);
  }

}


@media (max-width: 900px) {

  .desktop-nav {
    display: none;
  }

  .hero-container {
    grid-template-columns: 1fr;

    text-align: center;
  }

  .hero-content {
    max-width: 700px;

    margin: auto;
  }

  .hero-description {
    margin-left: auto;

    margin-right: auto;
  }

  .hero-buttons {
    justify-content: center;
  }

  .hero-trust {
    justify-content: center;
  }

  .hero-visual {
    max-width: 600px;

    width: 100%;

    margin: auto;
  }

  .steps-container {
    grid-template-columns: 1fr;

    gap: 15px;
  }

  .step-line {
    display: none;
  }

  .footer-container {
    grid-template-columns: 1fr;
  }

}


@media (max-width: 650px) {

  .navbar {
    height: 68px;
  }

  .nav-container {
    padding: 0 17px;
  }

  .nav-report-btn {
    display: none;
  }

  .brand-name {
    font-size: 13px;
  }

  .hero-container {
    padding: 65px 20px 40px;
  }

  .hero-title {
    font-size: 49px;

    letter-spacing: -2.5px;
  }

  .hero-description {
    font-size: 14px;
  }

  .hero-buttons {
    flex-direction: column;

    width: 100%;
  }

  .primary-btn,
  .secondary-btn {
    width: 100%;
  }

  .hero-bottom {
    grid-template-columns: 1fr;

    padding: 25px 20px;

    box-sizing: border-box;
  }

  .dashboard-card {
    padding: 18px;
  }

  .mini-stats {
    gap: 8px;
  }

  .mini-stat {
    padding: 11px;
  }

  .issue-item {
    gap: 7px;
  }

  .issue-info strong {
    font-size: 10px;
  }

  .status {
    font-size: 7px;

    padding: 4px 6px;
  }

  .section {
    padding: 75px 20px;
  }

  .feature-grid {
    grid-template-columns: 1fr;
  }

  .cta-section {
    padding: 60px 20px;
  }

  .cta-container {
    padding: 32px 25px;

    flex-direction: column;

    align-items: flex-start;
  }

  .cta-content {
    align-items: flex-start;
  }

  .cta-content h2 {
    font-size: 27px;
  }

  .cta-btn {
    width: 100%;
  }

  .footer {
    padding-left: 20px;

    padding-right: 20px;
  }

  .footer-links {
    grid-template-columns: 1fr 1fr;
  }

  .footer-bottom {
    flex-direction: column;

    gap: 8px;
  }

}


@media (max-width: 420px) {

  .hero-title {
    font-size: 42px;
  }

  .dashboard-header h3 {
    font-size: 17px;
  }

  .mini-stat strong {
    font-size: 16px;
  }

  .footer-links {
    grid-template-columns: 1fr;
  }

}

</style>