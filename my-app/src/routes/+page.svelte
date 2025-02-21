<script>
    import { Navbar, NavbarBrand, Nav, NavItem, NavLink, Container, Button, Row, Col, Card, CardBody, CardTitle, CardText } from '@sveltestrap/sveltestrap';
</script>

<!-- Navbar -->
<Navbar color="dark" dark expand="md" class="fixed-top shadow">
  <Container class="d-flex justify-content-between align-items-center">
    <NavbarBrand href="/">TechConf 2025</NavbarBrand>
    <div class="d-flex align-items-center">
      <Nav class="me-4" navbar>
        <NavItem><NavLink href="/speakers">Speakers</NavLink></NavItem>
        <NavItem><NavLink href="/schedule">Schedule</NavLink></NavItem>
        <NavItem><NavLink href="/sponsors">Sponsors</NavLink></NavItem>
        <NavItem><NavLink href="/about">About</NavLink></NavItem>
        <NavItem><NavLink href="/contact">Contact</NavLink></NavItem>
      </Nav>
    </div>
  </Container>
</Navbar>

<!-- Hero Section -->
<section class="hero text-center d-flex flex-column justify-content-center align-items-center">
  <div class="overlay"></div>
  <div class="content">
    <h1 class="display-3">TechConf 2025</h1>
    <p class="lead">Innovate. Inspire. Impact.</p>
    <Button color="primary" size="lg" href="/register">Register Now</Button>
  </div>
</section>

<!-- Featured Keynote Speaker Section -->
<Container id="speakers" class="content-section">
    <h2 class="text-center mb-4">Keynote Speaker</h2>
    <Row class="justify-content-center">
      <Col md="6" lg="4">
        <Card class="shadow">
          <img src="/keyspeaker.jpeg" alt="Dr. John Doe - AI & Robotics Expert" class="card-img-top speaker-img">
          <CardBody class="text-center">
            <CardTitle tag="h4">Dr. John Doe</CardTitle>
            <CardText>AI & Robotics Expert</CardText>
          </CardBody>
        </Card>
      </Col>
    </Row>
  </Container>
<!-- Extra Section to Ensure Scroll -->
<Container id="schedule" class="content-section">
  <h2 class="text-center mb-4">Conference Schedule</h2>
  <p class="text-center">Details coming soon...</p>
</Container>

<Container id="sponsors" class="content-section">
  <h2 class="text-center mb-4">Sponsors</h2>
  <p class="text-center">Exciting partnerships to be announced!</p>
</Container>

<!-- Styles -->
<style>
  /* Ensure smooth scrolling */
  html, body {
    height: 100%;
    overflow-x: hidden;
    scroll-behavior: smooth;
  }

  /* Hero Section */
  .hero {
    min-height: 90vh; /* Instead of 100vh */
    width: 100%;
    background: url('/hero-bg.webp') center/cover no-repeat;
    position: relative;
    text-align: center;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    padding: 100px 20px 20px; /* Prevent navbar overlap */
  }

  /* Overlay for better text contrast */
  .hero .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.6);
  }

  /* Hero content */
  .hero .content {
    position: relative;
    z-index: 2;
  }

  /* Ensure navbar doesn't overlap */
  .content-section {
    padding: 120px 20px;
  }

  /* Fixed Navbar */
  .fixed-top {
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  }
  /* Speaker image */
  .speaker-img {
    height: 350px; /* Adjust height */
    object-fit: cover; /* Maintain aspect ratio */
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
  }
</style>
