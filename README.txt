================================================================================
      LO TRINH ANGULAR 2 TUAN CHO FLUTTER DEVELOPER (VAO CODEBASE NHANH)
================================================================================

Tac gia: Tai cau truc cho Flutter Developer chuyen sang Angular
Ngay cap nhat: 2026-04-03
Muc tieu: Trong 2 tuan, doc duoc codebase Angular hien dai, them duoc feature vua,
          va fix duoc bug pho bien ma khong sa vao qua nhieu ly thuyet nen.

================================================================================
TOM TAT DINH HUONG
================================================================================

- Day la 1 recommended path duy nhat cho 14 ngay.
- Mac dinh dung Angular hien dai:
  + standalone components
  + control flow moi: @if, @for
  + signals cho component/app state
  + reactive forms
  + functional guards/interceptors
- RxJS rat quan trong cho async flows, HTTP va UI streams, nhung khong phai
  bai dau tien de viet feature.
- Template-driven forms, BehaviorSubject service state, NgRx, utility types nang
  cao va chi tiet ve NgModule duoc chuyen sang OPTIONAL/APPENDIX.

================================================================================
AI PHU HOP VOI LO TRINH NAY
================================================================================

Gia dinh ban da co:
- Dart, async/await, OOP
- State management co ban trong Flutter
- Tu duy widget tree va tach feature

Gia dinh ban con yeu:
- HTML/CSS
- TypeScript idioms
- Mental model Angular template + DI + router + RxJS

================================================================================
MAPPING TU DUY: FLUTTER -> ANGULAR
================================================================================

Widget              -> Component
build()             -> Template HTML
setState()          -> cap nhat state; template phan ung tu dong
ValueNotifier       -> signal()
Provider / GetIt    -> service + dependency injection
GoRouter            -> Angular Router
Stream              -> Observable
Form + controllers  -> Reactive Forms
Bloc/Riverpod       -> NgRx / Signals + services

Ghi nho:
- Signals la API state ro rang hon cho Angular moi.
- Observable dung cho async, HTTP, event stream, search/debounce, combine flows.

================================================================================
LO TRINH CORE 14 NGAY
================================================================================

Ngay 1 - TS essentials + doc cau truc app
- 001_typescript_cho_dart_dev/02_kieu_du_lieu_va_bien
- 001_typescript_cho_dart_dev/03_interface_va_type
- 001_typescript_cho_dart_dev/07_module_system
- 002_angular_cli_va_project_setup/01_cai_dat_angular_cli
- 002_angular_cli_va_project_setup/02_cau_truc_du_an

Ket qua can dat:
- Doc duoc app.component, app.config, app.routes, service, model
- Hieu strict null, interface/type, import/export
- Doc duoc loi type pho bien ma khong hoang

Optional practice:
- 001_typescript_cho_dart_dev/02_kieu_du_lieu_va_bien/thuc_hanh.txt
- 001_typescript_cho_dart_dev/03_interface_va_type/thuc_hanh.txt
- 002_angular_cli_va_project_setup/01_cai_dat_angular_cli/thuc_hanh.txt

Ngay 2 - Component, template, control flow, local signals
- 003_component_co_ban/01_tao_component
- 004_template_va_data_binding/01_interpolation_va_property_binding
- 004_template_va_data_binding/02_event_binding
- 005_directives/01_structural_directives
- 011_state_management/03_signals   <- hoc som, khong doi den chuong 11

Ket qua can dat:
- Viet duoc component standalone don gian
- Hieu data di tu state -> template -> event -> update state
- Dung duoc @if, @for, signal(), computed()

Optional practice:
- 003_component_co_ban/01_tao_component/thuc_hanh.txt

Ngay 3 - Input/output, services, DI, local feature flow
- 003_component_co_ban/03_input_output
- 006_services_va_dependency_injection/01_tao_service
- 006_services_va_dependency_injection/02_injection_tokens

Ket qua can dat:
- Tach duoc component cha/con
- Dua business logic vao service
- Hieu inject() va providedIn: 'root'

Optional practice:
- 001_typescript_cho_dart_dev/04_class_va_ke_thua/thuc_hanh.txt (on lai class/DI pattern)

Ngay 4 - Router va layout shell
- 007_routing_va_navigation/01_setup_routing
- 007_routing_va_navigation/02_route_params_va_query_params
- 007_routing_va_navigation/03_nested_routes_va_lazy_loading
- Lam bai: 007_routing_va_navigation/01_setup_routing/thuc_hanh.txt

Ket qua can dat:
- App co 3 routes + shell layout
- Doc duoc routerLink, router-outlet, route params

Ngay 5 - Reactive forms
- 008_forms/02_reactive_forms
- 008_forms/03_validation
- Lam bai: 008_forms/02_reactive_forms/thuc_hanh.txt

Ket qua can dat:
- Tao duoc reactive form co validation
- Submit du lieu va hien thi loi dung luc

Ngay 6 - HTTP, interceptor, loading/error/data state
- 009_http_va_api/01_http_client
- 009_http_va_api/02_interceptors
- 009_http_va_api/03_error_handling
- Lam bai: 009_http_va_api/01_http_client/thuc_hanh.txt

Ket qua can dat:
- Goi API bang HttpClient
- Them auth/logging interceptor
- Bieu dien loading, error, data ro rang trong component

Ngay 7 - RxJS du dung cho feature thuc
- 010_rxjs_va_reactive_programming/01_observable_co_ban
- 010_rxjs_va_reactive_programming/02_operators_thuong_dung
- 010_rxjs_va_reactive_programming/04_patterns_thuc_te
- Lam bai: 010_rxjs_va_reactive_programming/04_patterns_thuc_te/thuc_hanh.txt

Tap trung vao:
- map
- switchMap
- debounceTime
- catchError
- combineLatest
- takeUntilDestroyed

Ngay 8 - Signals o service layer + persistence
- 011_state_management/03_signals
- Lam bai: 011_state_management/03_signals/thuc_hanh.txt

Ket qua can dat:
- Biet khi nao dung signal, khi nao dung Observable
- Viet duoc signal service co computed selectors
- Luu/restore state tu localStorage

Ngay 9-11 - Todo app end-to-end
- 013_project_thuc_te/01_todo_app
- Lam bai: 013_project_thuc_te/01_todo_app/thuc_hanh.txt

Phai dat 3 moc:
- Ngay 9: list + add + toggle + filter
- Ngay 10: edit + delete + clear completed
- Ngay 11: localStorage + polish + tach component

Ngay 12 - Lazy loading, guards, Angular Material muc du dung
- 007_routing_va_navigation/03_nested_routes_va_lazy_loading
- 007_routing_va_navigation/04_guards
- 012_angular_material/01_setup_va_theming
- 012_angular_material/02_common_components
- 012_angular_material/03_layout_va_responsive

Ghi chu: Ngay nay co 5 bai doc, moi bai 10-20 phut (~60-90 phut tong).
Neu thay nang, chia thanh 2 buoi: guards/lazy-loading truoc, Material sau.
Hoac day Material sang ngay 13 va bo phan stretch feature.

Ngay 13 - Doc codebase Angular mau hoac them stretch feature
- Doc 1 feature Angular thuc te trong du an cong ty
- Hoac lam them filter/search/sort vao Todo app

Ngay 14 - Recap + bug-fix simulation
- Doc lai service, router, forms, HTTP, signals
- Tu fix 3 loi co chu dich:
  + route sai param
  + form submit khi invalid
  + list search khong debounce / khong xu ly error

================================================================================
CHECKPOINT BAT BUOC
================================================================================

Checkpoint 1 - Routing shell
- App standalone co 3 routes
- Co shared layout va router-outlet
- Co 1 route dung params hoac query params

Checkpoint 2 - Reactive form
- Form co Validators.required + it nhat 1 validator khac
- Khong submit neu invalid
- Co fake API submit flow

Checkpoint 3 - Search/list async
- Search co debounce
- Co loading, error, data state
- Khong subscribe thu cong linh tinh neu template da dung async pipe

Checkpoint 4 - Todo app bang signal service
- Signal service lam source of truth
- computed() cho filtered list / item count
- localStorage persistence

================================================================================
CORE VS OPTIONAL
================================================================================

CORE - Hoc trong 14 ngay
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
- 011/03 (hoc som tu ngay 2)
- 012/01, 012/02, 012/03
- 013/01

OPTIONAL / APPENDIX - Doc sau khi da lam xong core
- 001/01 setup moi truong neu ban chua dung TS/VS Code
- 001/04 class va ke thua
- 001/05 generics va utility types nang cao
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
- 010/03 subject va BehaviorSubject
- 011/01 service-based state voi RxJS
- 011/02 NgRx
- 013/02 ecommerce dashboard

================================================================================
HUONG DOC ANGULAR HIEN DAI
================================================================================

Nhung gi nen xem la mac dinh:
- standalone components thay vi bat dau tu NgModule
- provideRouter() thay vi RouterModule.forRoot() trong bai nhap mon
- provideHttpClient() + withInterceptors()
- @if, @for thay vi day qua som vao cu phap cu
- signals cho state noi bo va service-level state don gian

Nhung gi chi can biet de doc code, chua can master ngay:
- NgModule cu/legacy code
- BehaviorSubject state services
- NgRx
- decorators tu viet
- utility types nang cao, conditional types, mapped types sau

================================================================================
GHI CHU VE TOOLING
================================================================================

- ng new --standalone van la cach viet ro rang khi hoc, du Angular moi da uu tien
  standalone cho codebase moi.
- ng lint chi chay khi workspace da duoc cau hinh lint builder (thuong la
  angular-eslint). Khong mac dinh xem no la lenh luon co san trong moi project.
- ng serve cho feedback nhanh, nhung khong giu state nhu Flutter hot reload.
- Mot so file huong_dan goc dung tieng Viet co dau, mot so file moi sua dung
  khong dau. Noi dung khong khac nhau, chi la dinh dang text.

================================================================================
KET QUA MONG DOI SAU 2 TUAN
================================================================================

Ban co the:
- doc duoc cau truc feature Angular thuc te
- them route, form, service, HTTP call, interceptor, loading state
- phan biet signal va Observable
- fix duoc bug co ban trong component/template/router/forms/API flow
- tiep tuc hoc NgRx, Material nang cao, dashboard project ma khong bi ngop

================================================================================
