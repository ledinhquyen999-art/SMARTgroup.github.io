---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-08-13
type: landing

design:
  spacing: '5rem'

sections:
  # ─────────────────────────────────────────────
  # HERO — giới thiệu nhóm nghiên cứu
  # ─────────────────────────────────────────────
  - block: hero
    id: intro
    content:
      eyebrow: 'Trường Đại học Bách khoa, Đại học Đà Nẵng'
      title: 'Nhóm nghiên cứu [SMART]'
      text: |-
        <!-- TODO: viết 1-2 câu mô tả sứ mệnh / lĩnh vực nghiên cứu chính của nhóm -->
        Chúng tôi là nhóm nghiên cứu khoa học quy tụ giảng viên và sinh viên cùng
        theo đuổi các hướng nghiên cứu ứng dụng công nghệ. Cập nhật đoạn giới thiệu
        này để mô tả chính xác sứ mệnh của nhóm.
      primary_action:
        text: Xem thành viên
        url: '#team'
        icon: hero/user-group
      secondary_action:
        text: Công bố khoa học
        url: '#papers'
    design:
      layout: centered
      size: default
      background:
        gradient_mesh:
          enable: true

  # ─────────────────────────────────────────────
  # HƯỚNG NGHIÊN CỨU — TODO: thay bằng hướng nghiên cứu thật của nhóm
  # ─────────────────────────────────────────────
  - block: research-areas
    id: research
    content:
      title: 'Hướng nghiên cứu'
      subtitle: '# TODO: cập nhật các hướng nghiên cứu chính'
      text: ''
      items:
        - name: '# TODO: Hướng nghiên cứu 1'
          description: 'Mô tả ngắn gọn (50-100 từ) về hướng nghiên cứu này, các bài toán đang giải quyết.'
          icon: hero/cpu-chip
          gradient: from-primary-400 to-secondary-400
          status: active
        - name: '# TODO: Hướng nghiên cứu 2'
          description: 'Mô tả ngắn gọn (50-100 từ) về hướng nghiên cứu này, các bài toán đang giải quyết.'
          icon: hero/beaker
          gradient: from-blue-400 to-purple-500
          status: active
        - name: '# TODO: Hướng nghiên cứu 3'
          description: 'Mô tả ngắn gọn (50-100 từ) về hướng nghiên cứu này, các bài toán đang giải quyết.'
          icon: hero/light-bulb
          gradient: from-orange-400 to-red-500
          status: emerging
    design:
      layout: cards

  # ─────────────────────────────────────────────
  # THÀNH VIÊN — lấy dữ liệu từ data/authors/*.yaml (user_groups: Thành viên)
  # ─────────────────────────────────────────────
  - block: team-showcase
    id: team
    content:
      title: 'Thành viên nhóm'
      subtitle: 'Gặp gỡ các thành viên'
      text: ''
      user_groups:
        - Thành viên
      sort_by: name_family
      sort_ascending: true
      cta:
        text: Gia nhập nhóm
        url: '#contact'
        icon: hero/user-plus
    design:
      show_role: true
      show_organizations: true
      show_interests: false
      show_social: true
      align: center
      max_columns: 4
      show_empty_groups: false

  # ─────────────────────────────────────────────
  # CÔNG BỐ KHOA HỌC — thêm bài báo tại content/publications/<ten-bai-bao>/index.md
  # ─────────────────────────────────────────────
  - block: collection
    id: papers
    content:
      title: Công bố khoa học nổi bật
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: Công bố khoa học gần đây
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation

  # ─────────────────────────────────────────────
  # TIN TỨC — thêm bài viết tại content/post/<ten-bai-viet>/index.md
  # ─────────────────────────────────────────────
  - block: collection
    id: news
    content:
      title: Tin tức & Hoạt động
      subtitle: ''
      text: ''
      page_type: blog
      count: 6
      filters:
        author: ''
        category: ''
        tag: ''
        exclude_featured: false
        exclude_future: false
        exclude_past: false
      offset: 0
      order: desc
    design:
      view: card
      spacing:
        padding: [0, 0, 0, 0]

  # ─────────────────────────────────────────────
  # LIÊN HỆ
  # ─────────────────────────────────────────────
  - block: contact-info
    id: contact
    content:
      title: 'Liên hệ với chúng tôi'
      subtitle: '# TODO: cập nhật thông tin liên hệ bên dưới'
      visit_title: 'Địa chỉ'
      connect_title: 'Kết nối'
      address:
        lines:
          - 'Trường Đại học Bách khoa'
          - 'Đại học Đà Nẵng'
          - '# TODO: số nhà, đường, quận/thành phố'
      email: '# TODO@example.com'
      social: []
      prospective:
        title: 'Bạn muốn gia nhập nhóm?'
        text: 'Nếu bạn quan tâm đến các hướng nghiên cứu của chúng tôi, hãy liên hệ với chúng tôi qua email.'
        button:
          text: 'Liên hệ ngay'
          url: 'mailto:# TODO@example.com'
      show_form: false
---
