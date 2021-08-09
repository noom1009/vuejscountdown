<template>
  <div class="row">
    <div class="col-12">
      <nav class="navbar navbar-expand navbar-primary navbar-dark">
      <a href="/" class="navbar-brand">&nbsp;&nbsp;
        <span class="brand-text font-weight-light">สลากพารวย</span>
      </a>
        <ul class="navbar-nav ml-auto">
          <li class="nav-item d-none d-sm-inline-block">
            <a href="/" class="nav-link">
            <i class="fas fa-home"></i>&nbsp;&nbsp;หน้าหลัก</a>
          </li>
          <li class="nav-item d-none d-sm-inline-block">
            <a href="#" class="nav-link">
              <i class="fas fa-users"></i>&nbsp;&nbsp;สมัครสมาชิก</a>
          </li>
          <li class="nav-item d-none d-sm-inline-block">
            <a href="#" class="nav-link">
              <i class="fas fa-user-lock"></i>&nbsp;&nbsp;ตู้เซพสมาชิก</a>
          </li>
          <li class="nav-item d-none d-sm-inline-block">
            <a href="#" class="nav-link">
              <i class="far fa-comments"></i>&nbsp;&nbsp;ติดต่อเรา</a>
          </li>          
          <li class="nav-item dropdown">
            <a class="nav-link" data-widget="dropdown" href="#">
              <i class="fas fa-shopping-cart"></i>
              <span class="badge badge-danger navbar-badge">3</span>
              &nbsp;ตะกร้า
            </a>
            <div class="dropdown-menu dropdown-menu-lg dropdown-menu-right">
              <a href="#" class="dropdown-item">
                <div class="media">
                  <img
                    src="/dist/img/user1-128x128.jpg"
                    alt="User Avatar"
                    class="img-size-50 mr-3 img-circle"
                  />
                  <div class="media-body">
                    <h3 class="dropdown-item-title">
                      Brad Diesel
                      <span class="float-right text-sm text-danger"
                        ><i class="fas fa-star"></i
                      ></span>
                    </h3>
                    <p class="text-sm">Call me whenever you can</p>
                    <p class="text-sm text-muted">
                      <i class="far fa-clock mr-1"></i> 4 Hours Ago
                    </p>
                  </div>
                </div>
              </a>
              <div class="dropdown-divider"></div>
              <a href="#" class="dropdown-item dropdown-footer"
                >See All Messages</a
              >
            </div>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>
