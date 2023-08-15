# Progressive-Phase-Timeline-with-Visual-Indicators
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css"> <!-- Font Awesome CSS -->
  <style>
    .outer-container {
      background: #f5f5f5;
      padding: 20px;
    }
  
    .timeline {
      position: relative;
    }

    .timeline::before {
      content: '';
      position: absolute;
      top: 0;
      left: 50%;
      width: 2px;
      height: calc(100% - 20px);
      background-color: #ccc;
      transform: translateX(-50%);
      z-index: -1;
    }

    .timeline-event {
      position: relative;
      margin-bottom: 40px;
      width: 110%; /* Adjust the width as needed */
      margin-left: auto;
      margin-right: auto;
      left: -15px;
    }

    .timeline-event::before {
      content: '';
      position: absolute;
      top: 50%;
      left: -10px;
      width: 20px;
      height: 20px;
      background-color: #ccc;
      border-radius: 50%;
      transform: translateY(-50%);
    }

    .timeline-event-content {
      position: relative;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      display: flex;
      flex-wrap: wrap;
      justify-content: flex-start;
      align-items: flex-start;
      border-radius: 10px; /* Added border radius */
      background: linear-gradient(2deg, #0f335e, #010408);
    }

    .custom-h4 {
      font-weight: bold;
      font-size: 18px;
      margin-top: 0;
      margin-bottom: 10px;
      color: #FFF;
    }

    .custom-h4 .fa {
      margin-right: 5px;
    }

    .timeline-description {
      font-size: 14px;
      margin-bottom: 10px;
      color: #FFF;
    }

    .timeline-description p {
      margin-bottom: 0;
    }

    .timeline-description-left {
      width: 50%;
      float: left;
      margin-right: 10px;
      color: #FFF;
      font-size: 13px;
    }

    .timeline-event-content img {
      max-width: 50%;
      height: 40px;
      width: 80%;
      margin: 0 auto;
      display: block;
      margin-bottom: 20px;
    }

    .progress-bar-container {
      height: 10px;
      background-color: #f9f9f9;
      border-radius: 5px;
      overflow: hidden;
      margin-bottom: 10px;
      width: 100%; /* Adjust the width as needed */
    }

    .progress-bars-container {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding-top: 20px;
      padding-left: 10px;
    }

    .progress-bar-container + .progress-bar-container {
      margin-top: 15px; /* Additional margin for the second progress bar */
    }

    .progress-bar-fill {
      height: 100%;
      width: 0; /* Initial width */
      background-color: #a0d8ef; /* Default fill color */
    }

    .dropdown-content {
      display: none;
    }

    .custom-h4 .dropdown-arrow {
      cursor: pointer;
      margin-left: 10px;
    }

    .custom-h4 .dropdown-arrow.rotate {
      transform: rotate(180deg);
    }

    .timeline-event-content.show .dropdown-content {
      display: block;
    }
  </style>
</head>
<body>
  <div class="outer-container">
    <div class="container">
      <div class="row">
        <div class="col-md-6 offset-md-3">
          <div class="timeline">
            <div class="timeline-event phase1">
              <div class="timeline-event-content">
                <div class="custom-h4">
                  <i class="fas fa-chart-line"></i> <!-- Font Awesome icon -->
                  Phase 1<br>
                  Business Understanding
                  <span class="dropdown-arrow">&#9662;</span>
                </div>
                <div class="dropdown-content">
                  <img src="http://dataastraa.com/wp-content/uploads/2023/07/Business-Understanding.jpg" alt="Phase 1 Image" style="max-width: 100%; height: auto;">
                  <div class="timeline-description-left">
                    <p>Understand clients' Business Model</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 10%; background-color: #a0d8ef;"></div>
                    </div>
                  </div>
                  <div class="timeline-description-left">
                    <p>Requirement Mapping on Client's needs</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 14%; background-color: #a0d8ef;"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="timeline-event phase1">
              <div class="timeline-event-content">
                <div class="custom-h4">
                  <i class="fas fa-cogs"></i> <!-- Font Awesome icon -->
                  Phase 2<br>
                  System Design
                  <span class="dropdown-arrow">&#9662;</span>
                </div>
                <div class="dropdown-content">
                  <img src="http://dataastraa.com/wp-content/uploads/2023/07/System-Design.jpg" alt="Phase 1 Image" style="max-width: 100%; height: auto;">
                  <div class="timeline-description-left">
                    <p>Learn solution-oriented system design approach</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 15%; background-color: #63c1e5; margin-left: 14%;"></div>
                    </div>
                  </div>
                  <div class="timeline-description-left">
                    <p>Drawing board system design sessions</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 20%; background-color: #63c1e5; margin-left: 14%;"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="timeline-event phase1">
              <div class="timeline-event-content">
                <div class="custom-h4">
                  <i class="fas fa-database"></i> <!-- Font Awesome icon -->
                  Phase 3<br>
                  Data Wrangling
                  <span class="dropdown-arrow">&#9662;</span>
                </div>
                <div class="dropdown-content">
                  <img src="http://dataastraa.com/wp-content/uploads/2023/07/Data-Wraggling.jpg" alt="Phase 1 Image" style="max-width: 100%; height: auto;">
                  <div class="timeline-description-left">
                    <p>Build Data Pipeline for Business Process</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 25%; background-color: #20a8dc; margin-left: 34%;"></div>
                    </div>
                  </div>
                  <div class="timeline-description-left">
                    <p>Learn How to prepare real-world data</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 28%; background-color: #20a8dc; margin-left: 34%;"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="timeline-event phase1">
              <div class="timeline-event-content">
                <div class="custom-h4">
                  <i class="fas fa-chart-bar"></i> <!-- Font Awesome icon -->
                  Phase 4<br>
                  BI Dashboards
                  <span class="dropdown-arrow">&#9662;</span>
                </div>
                <div class="dropdown-content">
                  <img src="http://dataastraa.com/wp-content/uploads/2023/07/BI-dashboard.jpg" alt="Phase 1 Image" style="max-width: 100%; height: auto;">
                  <div class="timeline-description-left">
                    <p>Instructor-led guided training from industry experts</p>
                  </div>
                  <div class="progress-bars-container">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 32%; background-color: #1c96c5; margin-left: 62%;"></div>
                    </div>
                  </div>
                  <div class="timeline-description-left">
                    <p>Apply all the concepts learned to solve real-world business problems</p>
                  </div>
                  <div class="progress-bars-container" style="padding-top: 40px;">
                    <div class="progress-bar-container">
                      <div class="progress-bar-fill" style="width: 38%; background-color: #1c96c5; margin-left: 62%;"></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Include Bootstrap JavaScript and Font Awesome JavaScript -->
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/js/all.min.js"></script> <!-- Font Awesome JavaScript -->
  <script>
    document.addEventListener('DOMContentLoaded', function() {
      var dropdownArrows = document.querySelectorAll('.dropdown-arrow');
      dropdownArrows.forEach(function(arrow) {
        arrow.addEventListener('click', function() {
          var timelineEventContent = this.parentNode.parentNode;
          timelineEventContent.classList.toggle('show');
          this.classList.toggle('rotate');
        });
      });
    });
  </script>
</body>
</html>
