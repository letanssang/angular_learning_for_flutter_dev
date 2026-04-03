================================================================================
      LỘ TRÌNH ANGULAR 2 TUẦN CHO FLUTTER DEVELOPER (VÀO CODEBASE NHANH)
================================================================================

Tác giả: Tái cấu trúc cho Flutter Developer chuyển sang Angular
Ngày cập nhật: 2026-04-03
Mục tiêu: Trong 2 tuần, đọc được codebase Angular hiện đại, thêm được feature vừa,
          và fix được bug phổ biến mà không sa vào quá nhiều lý thuyết nền.

================================================================================
TÓM TẮT ĐỊNH HƯỚNG
================================================================================

- Đây là 1 recommended path duy nhất cho 14 ngày.
- Mặc định dùng Angular hiện đại:
  + standalone components
  + control flow mới: @if, @for
  + signals cho component/app state
  + reactive forms
  + functional guards/interceptors
- RxJS rất quan trọng cho async flows, HTTP và UI streams, nhưng không phải
  bài đầu tiên để viết feature.
- Template-driven forms, BehaviorSubject service state, NgRx, utility types nâng
  cao và chi tiết về NgModule được chuyển sang OPTIONAL/APPENDIX.

================================================================================
AI PHÙ HỢP VỚI LỘ TRÌNH NÀY
================================================================================

Giả định bạn đã có:
- Dart, async/await, OOP
- State management cơ bản trong Flutter
- Tư duy widget tree và tách feature

Giả định bạn còn yếu:
- HTML/CSS
- TypeScript idioms
- Mental model Angular template + DI + router + RxJS

================================================================================
MAPPING TƯ DUY: FLUTTER -> ANGULAR
================================================================================

Widget              -> Component
build()             -> Template HTML
setState()          -> cập nhật state; template phản ứng tự động
ValueNotifier       -> signal()
Provider / GetIt    -> service + dependency injection
GoRouter            -> Angular Router
Stream              -> Observable
Form + controllers  -> Reactive Forms
Bloc/Riverpod       -> NgRx / Signals + services

Ghi nhớ:
- Signals là API state rõ ràng hơn cho Angular mới.
- Observable dùng cho async, HTTP, event stream, search/debounce, combine flows.

================================================================================
LỘ TRÌNH CORE 14 NGÀY
================================================================================

Ngày 1 - TS essentials + đọc cấu trúc app
- 001_typescript_cho_dart_dev/02_kieu_du_lieu_va_bien
- 001_typescript_cho_dart_dev/03_interface_va_type
- 001_typescript_cho_dart_dev/07_module_system
- 002_angular_cli_va_project_setup/01_cai_dat_angular_cli
- 002_angular_cli_va_project_setup/02_cau_truc_du_an

Kết quả cần đạt:
- Đọc được app.component, app.config, app.routes, service, model
- Hiểu strict null, interface/type, import/export
- Đọc được lỗi type phổ biến mà không hoảng

Ngày 2 - Component, template, control flow, local signals
- 003_component_co_ban/01_tao_component
- 004_template_va_data_binding/01_interpolation_va_property_binding
- 004_template_va_data_binding/02_event_binding
- 005_directives/01_structural_directives
- 011_state_management/03_signals   <- học sớm, không đợi đến chương 11

Kết quả cần đạt:
- Viết được component standalone đơn giản
- Hiểu data đi từ state -> template -> event -> update state
- Dùng được @if, @for, signal(), computed()

Ngày 3 - Input/output, services, DI, local feature flow
- 003_component_co_ban/03_input_output
- 006_services_va_dependency_injection/01_tao_service
- 006_services_va_dependency_injection/02_injection_tokens

Kết quả cần đạt:
- Tách được component cha/con
- Đưa business logic vào service
- Hiểu inject() và providedIn: 'root'

Ngày 4 - Router và layout shell
- 007_routing_va_navigation/01_setup_routing
- 007_routing_va_navigation/02_route_params_va_query_params
- 007_routing_va_navigation/03_nested_routes_va_lazy_loading
- Làm bài: 007_routing_va_navigation/01_setup_routing/thuc_hanh.txt

Kết quả cần đạt:
- App có 3 routes + shell layout
- Đọc được routerLink, router-outlet, route params

Ngày 5 - Reactive forms
- 008_forms/02_reactive_forms
- 008_forms/03_validation
- Làm bài: 008_forms/02_reactive_forms/thuc_hanh.txt

Kết quả cần đạt:
- Tạo được reactive form có validation
- Submit dữ liệu và hiển thị lỗi đúng lúc

Ngày 6 - HTTP, interceptor, loading/error/data state
- 009_http_va_api/01_http_client
- 009_http_va_api/02_interceptors
- 009_http_va_api/03_error_handling
- Làm bài: 009_http_va_api/01_http_client/thuc_hanh.txt

Kết quả cần đạt:
- Gọi API bằng HttpClient
- Thêm auth/logging interceptor
- Biểu diễn loading, error, data rõ ràng trong component

Ngày 7 - RxJS đủ dùng cho feature thực
- 010_rxjs_va_reactive_programming/01_observable_co_ban
- 010_rxjs_va_reactive_programming/02_operators_thuong_dung
- 010_rxjs_va_reactive_programming/04_patterns_thuc_te
- Làm bài: 010_rxjs_va_reactive_programming/04_patterns_thuc_te/thuc_hanh.txt

Tập trung vào:
- map
- switchMap
- debounceTime
- catchError
- combineLatest
- takeUntilDestroyed

Ngày 8 - Signals ở service layer + persistence
- 011_state_management/03_signals
- Làm bài: 011_state_management/03_signals/thuc_hanh.txt

Kết quả cần đạt:
- Biết khi nào dùng signal, khi nào dùng Observable
- Viết được signal service có computed selectors
- Lưu/restore state từ localStorage

Ngày 9-11 - Todo app end-to-end
- 013_project_thuc_te/01_todo_app
- Làm bài: 013_project_thuc_te/01_todo_app/thuc_hanh.txt

Phải đạt 3 mốc:
- Ngày 9: list + add + toggle + filter
- Ngày 10: edit + delete + clear completed
- Ngày 11: localStorage + polish + tách component

Ngày 12 - Lazy loading, guards, Angular Material mức đủ dùng
- 007_routing_va_navigation/03_nested_routes_va_lazy_loading
- 007_routing_va_navigation/04_guards
- 012_angular_material/01_setup_va_theming
- 012_angular_material/02_common_components
- 012_angular_material/03_layout_va_responsive

Ngày 13 - Đọc codebase Angular mẫu hoặc thêm stretch feature
- Đọc 1 feature Angular thực tế trong dự án công ty
- Hoặc làm thêm filter/search/sort vào Todo app

Ngày 14 - Recap + bug-fix simulation
- Đọc lại service, router, forms, HTTP, signals
- Tự fix 3 lỗi có chủ đích:
  + route sai param
  + form submit khi invalid
  + list search không debounce / không xử lý error

================================================================================
CHECKPOINT BẮT BUỘC
================================================================================

Checkpoint 1 - Routing shell
- App standalone có 3 routes
- Có shared layout và router-outlet
- Có 1 route dùng params hoặc query params

Checkpoint 2 - Reactive form
- Form có Validators.required + ít nhất 1 validator khác
- Không submit nếu invalid
- Có fake API submit flow

Checkpoint 3 - Search/list async
- Search có debounce
- Có loading, error, data state
- Không subscribe thủ công linh tinh nếu template đã dùng async pipe

Checkpoint 4 - Todo app bằng signal service
- Signal service làm source of truth
- computed() cho filtered list / item count
- localStorage persistence

================================================================================
CORE VS OPTIONAL
================================================================================

CORE - Học trong 14 ngày
- 001/02, 001/03, 001/07
- 002/01, 002/02
- 003/01, 003/03
- 004/01, 004/02, 004/03
- 005/01
- 006/01, 006/02
- 007/01, 007/02, 007/03, 007/04
- 008/02, 008/03
- 009/01, 009/02, 009/03
- 010/01, 010/02, 010/04
- 011/03 (học sớm từ ngày 2)
- 012/01, 012/02, 012/03
- 013/01

OPTIONAL / APPENDIX - Đọc sau khi đã làm xong core
- 001/01 setup môi trường nếu bạn chưa dùng TS/VS Code
- 001/04 class và kế thừa
- 001/05 generics và utility types nâng cao
- 001/06 decorators
- 003/02 lifecycle hooks
- 003/04 content projection
- 003/05 view encapsulation
- 004/04 template reference variables
- 004/05 pipes
- 005/02 attribute directives
- 005/03 custom directive
- 006/03 hierarchical injection
- 008/01 template-driven forms
- 010/03 subject và BehaviorSubject
- 011/01 service-based state với RxJS
- 011/02 NgRx
- 013/02 ecommerce dashboard

================================================================================
HƯỚNG ĐỌC ANGULAR HIỆN ĐẠI
================================================================================

Những gì nên xem là mặc định:
- standalone components thay vì bắt đầu từ NgModule
- provideRouter() thay vì RouterModule.forRoot() trong bài nhập môn
- provideHttpClient() + withInterceptors()
- @if, @for thay vì đẩy quá sớm vào cú pháp cũ
- signals cho state nội bộ và service-level state đơn giản

Những gì chỉ cần biết để đọc code, chưa cần master ngay:
- NgModule cũ/legacy code
- BehaviorSubject state services
- NgRx
- decorators tự viết
- utility types nâng cao, conditional types, mapped types sau

================================================================================
GHI CHÚ VỀ TOOLING
================================================================================

- ng new --standalone vẫn là cách viết rõ ràng khi học, dù Angular mới đã ưu tiên
  standalone cho codebase mới.
- ng lint chỉ chạy khi workspace đã được cấu hình lint builder (thường là
  angular-eslint). Không mặc định xem nó là lệnh luôn có sẵn trong mọi project.
- ng serve cho feedback nhanh, nhưng không giữ state như Flutter hot reload.

================================================================================
KẾT QUẢ MONG ĐỢI SAU 2 TUẦN
================================================================================

Bạn có thể:
- đọc được cấu trúc feature Angular thực tế
- thêm route, form, service, HTTP call, interceptor, loading state
- phân biệt signal và Observable
- fix được bug cơ bản trong component/template/router/forms/API flow
- tiếp tục học NgRx, Material nâng cao, dashboard project mà không bị ngợp

================================================================================
