# [Visual Studio SDK 기본 사항](inside-the-visual-studio-sdk.md)
# [Visual Studio Shell](visual-studio-shell.md)
# [사용자 설정 지원](support-for-user-settings.md)
# [Microsoft 도움말 뷰어 SDK](microsoft-help-viewer-sdk.md)
# [명령, 메뉴 및 도구 모음](commands-menus-and-toolbars.md)
## [VSPackage에서 사용자 인터페이스 요소를 추가하는 방법](how-vspackages-add-user-interface-elements.md)
## [Visual Studio 명령 테이블(.Vsct) 파일](visual-studio-command-table-dot-vsct-files.md)
### [.Vsct 파일 작성](authoring-dot-vsct-files.md)
### [XML 명령 테이블(.Vsct) 파일 디자인](designing-xml-command-table-dot-vsct-files.md)
### [방법: .Vsct 파일 만들기](how-to-create-a-dot-vsct-file.md)
### [VSCT 컴파일러 명령줄 플래그](vsct-compiler-command-line-flags.md)
## [기본 명령, 그룹 및 도구 모음 배치](default-command-group-and-toolbar-placement.md)
## [IDE 정의 명령, 메뉴 및 그룹](ide-defined-commands-menus-and-groups.md)
### [Visual Studio 메뉴의 GUID 및 ID](guids-and-ids-of-visual-studio-menus.md)
### [Visual Studio 도구 모음의 GUID 및 ID](guids-and-ids-of-visual-studio-toolbars.md)
### [Visual Studio 명령의 GUID 및 ID](guids-and-ids-of-visual-studio-commands.md)
## [명령 디자인](command-design.md)
### [구현](command-implementation.md)
### [가용성](command-availability.md)
### [라우팅 알고리즘](command-routing-algorithm.md)
### [배치 지침](command-placement-guidelines.md)
## [메뉴 및 도구 모음 명령 최적화](optimizing-menu-and-toolbar-commands.md)
## [명령을 사용 가능하게 지정](making-commands-available.md)
## [Interop 어셈블리를 사용하는 명령 및 메뉴](commands-and-menus-that-use-interop-assemblies.md)
### [Interop 어셈블리를 사용하여 명령 상태 결정](determining-command-status-by-using-interop-assemblies.md)
### [Interop 어셈블리의 명령 계약](command-contracts-in-interop-assemblies.md)
### [Interop 어셈블리 명령 처리기를 등록](registering-interop-assembly-command-handlers.md)
### [Visual Studio Interop 어셈블리 사용](using-visual-studio-interop-assemblies.md)
## [VSPackage의 명령 라우팅](command-routing-in-vspackages.md)
# [VSPackage](vspackages.md)
## [VSPackage 파일 위치를 VS Shell 지정](specifying-vspackage-file-location-to-the-vs-shell.md)
## [VSPackage의 리소스](resources-in-vspackages.md)
## [VSPackage의 보안 모범 사례](best-practices-for-security-in-vspackages.md)
## [VSPackage 등록](registering-vspackages.md)
# [문서 창](document-windows.md)
## [문서 테이블 실행](running-document-table.md)
### [RDT_ReadLock 사용법](rdt-readlock-usage.md)
### [지속성 및 실행 중인 문서 테이블](persistence-and-the-running-document-table.md)
## [지연된 문서 로드](delayed-document-loading.md)
# [레거시 언어 서비스 확장성](legacy-language-service-extensibility.md)
## [레거시 언어 서비스 마이그레이션](migrating-a-legacy-language-service.md)
## [레거시 언어 서비스 필수 항목](legacy-language-service-essentials.md)
## [레거시 언어 서비스 개발](developing-a-legacy-language-service.md)
### [레거시 언어 서비스 모델](model-of-a-legacy-language-service.md)
### [레거시 언어 서비스 인터페이스](legacy-language-service-interfaces.md)
### [레거시 언어 서비스 명령 가로채기](intercepting-legacy-language-service-commands.md)
#### [언어 서비스 필터에 대한 중요 명령](important-commands-for-language-service-filters.md)
### [레거시 언어 서비스 등록](registering-a-legacy-language-service2.md)
### [검사 목록: 레거시 언어 서비스 만들기](checklist-creating-a-legacy-language-service.md)
### [레거시 언어 서비스 기능](legacy-language-service-features2.md)
#### [레거시 언어 서비스의 구문 색 지정](syntax-coloring-in-a-legacy-language-service.md)
##### [구문 색 지정 구현](implementing-syntax-coloring.md)
##### [방법: 기본 제공 색 항목 사용](how-to-use-built-in-colorable-items.md)
##### [사용자 지정 색 항목](custom-colorable-items.md)
#### [레거시 언어 서비스의 자동 서식](automatic-formatting-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 매개 변수 정보](parameter-info-in-a-legacy-language-service1.md)
#### [레거시 언어 서비스의 문 완성](statement-completion-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 개요 표시 및 숨겨진 텍스트](outlining-and-hidden-text-in-a-legacy-language-service.md)
##### [방법: 레거시 언어 서비스의 개요 표시 지원](how-to-support-outlining-in-a-legacy-language-service.md)
##### [방법: 레거시 언어 서비스에서 숨겨진 텍스트 지원 제공](how-to-provide-hidden-text-support-in-a-legacy-language-service.md)
##### [방법: 레거시 언어 서비스에서 확장 개요 표시 지원 제공](how-to-provide-expanded-outlining-support-in-a-legacy-language-service.md)
#### [디버깅에 대한 언어 서비스 지원](language-service-support-for-debugging.md)
## [레거시 언어 서비스 구현](implementing-a-legacy-language-service1.md)
### [레거시 언어 서비스 개요](legacy-language-service-overview.md)
### [언어 서비스 구현](implementing-a-legacy-language-service2.md)
### [언어 서비스 등록](registering-a-legacy-language-service1.md)
### [레거시 언어 서비스 파서 및 검사기](legacy-language-service-parser-and-scanner.md)
### [연습: 레거시 언어 서비스 만들기](walkthrough-creating-a-legacy-language-service.md)
### [연습: 설치된 코드 조각 목록 가져오기(레거시 구현)](walkthrough-getting-a-list-of-installed-code-snippets-legacy-implementation.md)
### [레거시 언어 서비스 기능](legacy-language-service-features1.md)
#### [레거시 언어 서비스의 중괄호 일치](brace-matching-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 코드 주석 처리](commenting-code-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 사용자 지정 문서 속성](custom-document-properties-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 개요 표시](outlining-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 코드 서식 다시 지정](reformatting-code-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 코드 조각 지원](support-for-code-snippets-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 매개 변수 정보](parameter-info-in-a-legacy-language-service2.md)
#### [레거시 언어 서비스의 빠른 정보](quick-info-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 멤버 완성](member-completion-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 단어 완성](word-completion-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 자동 창 지원](support-for-the-autos-window-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 탐색 모음 지원](support-for-the-navigation-bar-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 구문 색 지정](syntax-colorizing-in-a-legacy-language-service.md)
#### [레거시 언어 서비스의 중단점 유효성 검사](validating-breakpoints-in-a-legacy-language-service.md)
## [기호 검색 도구 지원](supporting-symbol-browsing-tools.md)
### [방법: 개체 관리자에 라이브러리 등록](how-to-register-a-library-with-the-object-manager.md)
### [방법: 라이브러리에서 제공하는 기호 목록을 개체 관리자에 노출](how-to-expose-lists-of-symbols-provided-by-the-library-to-the-object-manager.md)
### [방법: 라이브러리의 기호 식별](how-to-identify-symbols-in-a-library.md)
# [프로젝트](projects.md)
## [새 프로젝트 생성: 내부 살펴보기, 1부](new-project-generation-under-the-hood-part-one.md)
## [새 프로젝트 생성: 내부 살펴보기, 2부](new-project-generation-under-the-hood-part-two.md)
## [프로젝트 형식](project-types.md)
### [Essentials](project-type-essentials.md)
### [프로젝트 형식 만들기](creating-project-types.md)
#### [프로젝트 형식 디자인 결정](project-type-design-decisions.md)
#### [검사 목록: 새 프로젝트 형식 만들기](checklist-creating-new-project-types.md)
#### [프로젝트 팩터리를 사용하여 프로젝트 인스턴스 만들기](creating-project-instances-by-using-project-factories.md)
#### [관리 패키지 프레임워크를 사용하여 프로젝트 형식 구현(C#)](using-the-managed-package-framework-to-implement-a-project-type-csharp.md)
#### [프로젝트 형식 등록](registering-a-project-type.md)
#### [프로젝트 지속성](project-persistence.md)
#### [MSBuild 사용](using-msbuild.md)
### [프로젝트 및 프로젝트 항목 템플릿 추가](adding-project-and-project-item-templates.md)
#### [프로젝트 컨텍스트](project-context.md)
#### [프로젝트 우선 순위](project-priority.md)
#### [기타 파일 프로젝트](miscellaneous-files-project.md)
#### [프로젝트 템플릿 및 항목 템플릿 등록](registering-project-and-item-templates.md)
#### [새 항목 추가 대화 상자에 항목 추가](adding-items-to-the-add-new-item-dialog-boxes.md)
#### [새 프로젝트 대화 상자에 디렉터리 추가](adding-directories-to-the-new-project-dialog-box.md)
#### [새 항목 추가 대화 상자에 디렉터리 추가](adding-directories-to-the-add-new-item-dialog-box.md)
#### [프로젝트 시스템 확장을 위한 IDE 정의 명령](ide-defined-commands-for-extending-project-systems.md)
#### [일반적으로 프로젝트를 확장하는 데 사용되는 개체에 대한 CATID](catids-for-objects-that-are-typically-used-to-extend-projects.md)
### [프로젝트 항목 열기 및 저장](opening-and-saving-project-items.md)
#### [파일 열기 명령을 사용하여 파일 표시](displaying-files-by-using-the-open-file-command.md)
#### [연결 프로그램 명령을 사용하여 파일 표시](displaying-files-by-using-the-open-with-command.md)
#### [표준 문서 저장](saving-a-standard-document.md)
#### [사용자 지정 문서 저장](saving-a-custom-document.md)
#### [프로젝트에서 파일을 여는 편집기 결정](determining-which-editor-opens-a-file-in-a-project.md)
### [구성 옵션 관리](managing-configuration-options.md)
#### [개요](configuration-options-overview.md)
#### [속성 페이지](property-pages.md)
#### [솔루션 구성](solution-configuration.md)
#### [프로젝트 구성 개체](project-configuration-object.md)
#### [빌드를 위한 프로젝트 구성](project-configuration-for-building.md)
#### [배포 관리를 위한 프로젝트 구성](project-configuration-for-managing-deployment.md)
#### [출력에 대한 프로젝트 구성](project-configuration-for-output.md)
### [소스 제어 지원](supporting-source-control.md)
#### [소스 제어 패키지 모델](model-for-source-control-packages.md)
#### [디자인 결정](source-control-design-decisions.md)
#### [구성 세부 정보](source-control-configuration-details.md)
#### [프로젝트 및 편집기에 대한 추가 지침](additional-source-control-guidelines-for-projects-and-editors.md)
#### [런타임 세부 정보](source-control-runtime-details.md)
### [프로젝트 중첩](nesting-projects.md)
#### [방법: 중첩된 프로젝트 구현](how-to-implement-nested-projects.md)
#### [중첩된 프로젝트 언로드 및 다시 로드에 대한 고려 사항](considerations-for-unloading-and-reloading-nested-projects.md)
#### [중첩된 프로젝트에 대한 마법사 지원](wizard-support-for-nested-projects.md)
#### [중첩된 프로젝트에 대한 명령 처리 구현](implementing-command-handling-for-nested-projects.md)
#### [중첩된 프로젝트에 대한 AddItem 필터링 대화 상자](filtering-the-additem-dialog-box-for-nested-projects.md)
### [프로젝트 업그레이드](upgrading-projects.md)
### [아키텍처](project-types-architecture.md)
#### [프로젝트 모델의 요소](elements-of-a-project-model.md)
#### [프로젝트 모델 핵심 구성 요소](project-model-core-components.md)
#### [프로젝트 형식을 만들어야 하는 경우](when-to-create-project-types.md)
#### [계층 구조 및 선택](hierarchies-and-selection.md)
##### [Visual Studio의 계층 구조](hierarchies-in-visual-studio.md)
##### [IDE의 선택 및 통화](selection-and-currency-in-the-ide.md)
##### [선택 컨텍스트 개체](selection-context-objects.md)
##### [사용자에 대한 피드백](feedback-to-the-user.md)
## [프로젝트 하위 형식](project-subtypes.md)
### [프로젝트 하위 형식 디자인](project-subtypes-design.md)
### [프로젝트 하위 형식의 초기화 시퀀스](initialization-sequence-of-project-subtypes.md)
### [프로젝트 하위 형식에 의해 확장된 속성 및 메서드](properties-and-methods-extended-by-project-subtypes.md)
### [MSBuild 프로젝트 파일의 데이터 유지](persisting-data-in-the-msbuild-project-file.md)
### [프로젝트 속성 사용자 인터페이스](project-property-user-interface.md)
### [기본 프로젝트의 개체 모델 확장](extending-the-object-model-of-the-base-project.md)
### [새 항목 추가 대화 상자에 적용](contributing-to-the-add-new-item-dialog-box.md)
## [웹 프로젝트](web-projects.md)
### [Essentials](web-project-essentials.md)
### [웹 사이트 지원](web-site-support.md)
#### [웹 사이트 지원 템플릿](web-site-support-templates.md)
#### [웹 사이트 지원 특성](web-site-support-attributes.md)
## [특수 배포 처리](handling-specialized-deployment.md)
## [자동화 모델에 적용](contributing-to-the-automation-model.md)
### [자동화 모델 개요](automation-model-overview.md)
### [VSPackage에 대한 자동화 제공](providing-automation-for-vspackages.md)
### [프로젝트 개체 노출](exposing-project-objects.md)
### [프로젝트 모델링](project-modeling.md)
### [이벤트 노출](exposing-events-in-the-visual-studio-sdk.md)
### [옵션 페이지의 자동화 지원](automation-support-for-options-pages.md)
### [코드에 대한 자동화 제공](providing-automation-for-code.md)
### [방법: Windows에 대한 자동화 제공](how-to-provide-automation-for-windows.md)
### [자동화 모델 사용](using-the-automation-model.md)
### [ 및 SelectedItem 개체 자동화](automation-for-configuration-and-selecteditem-objects.md)
# [솔루션](solutions.md)
## [개요](solutions-overview.md)
## [솔루션(.Sln) 파일](solution-dot-sln-file.md)
## [솔루션 사용자 옵션(.Suo) 파일](solution-user-options-dot-suo-file.md)
# [속성 확장](extending-properties.md)
## [속성 창 개요](properties-window-overview.md)
## [템플릿 정책 및 속성 창](template-policy-and-the-properties-window.md)
## [속성 창 필드 및 인터페이스](properties-window-fields-and-interfaces.md)
## [속성 창 개요 목록](properties-window-object-list.md)
## [속성 창 단추](properties-window-buttons.md)
## [속성 눈금 표시](properties-display-grid.md)
## [프로젝트 및 구성 속성 지원](support-for-project-and-configuration-properties.md)
# [옵션 및 옵션 페이지](options-and-options-pages.md)
## [옵션 페이지 만들기](creating-options-pages.md)
# [서비스 필수 항목](service-essentials.md)
## [사용 가능한 서비스 목록](list-of-available-services.md)
# [Visual Studio 디버거 확장성](../debugger/visual-studio-debugger-extensibility.md)
# [소스 제어](source-control.md)
## [Essentials](source-control-integration-essentials.md)
## [개요](source-control-integration-overview.md)
### [소스 제어의 새로운 기능](what-s-new-in-source-control.md)
## [소스 제어 플러그 인 만들기](creating-a-source-control-plug-in.md)
### [시작](getting-started-with-source-control-plug-ins.md)
#### [방법: 소스 제어 플러그 인 설치](how-to-install-a-source-control-plug-in.md)
#### [소스 제어 플러그 인 API 버전 1.3의 새로운 기능](what-s-new-in-the-source-control-plug-in-api-version-1-3.md)
#### [소스 제어 플러그 인 API 버전 1.2의 새로운 기능](what-s-new-in-the-source-control-plug-in-api-version-1-2.md)
##### [~SAK 파일 제거](elimination-of-tilde-sak-files.md)
##### [여러 프로젝트 연결 간 설정 적용](application-of-settings-across-multiple-project-connections.md)
##### [솔루션에 대한 부모 컨테이너 폴더 만들기](creating-parent-container-folders-for-solutions.md)
##### [로컬 프로젝트 폴더와 소스 제어 저장소의 선택적 비교](optional-comparison-of-local-project-folder-to-source-control-store.md)
##### [.Proj 및 .Sln 파일에서 소스 제어 정보 제거](removal-of-source-control-information-from-dot-proj-and-dot-sln-files.md)
### [아키텍처](source-control-plug-in-architecture.md)
### [소스 제어 플러그 인에 대한 테스트 가이드](test-guide-for-source-control-plug-ins.md)
#### [테스트 영역 1: 소스 제어에 추가/소스 제어에서 열기](test-area-1-add-to-open-from-source-control.md)
#### [테스트 영역 2: 소스 제어에서 가져오기](test-area-2-get-from-source-control.md)
#### [테스트 영역 3: 체크 아웃/체크 아웃 실행 취소](test-area-3-check-out-undo-checkout.md)
#### [테스트 영역 4: 체크 인](test-area-4-check-in.md)
#### [테스트 영역 5: 소스 제어 변경](test-area-5-change-source-control.md)
#### [테스트 영역 6: 삭제](test-area-6-delete.md)
#### [테스트 영역 7: 공유](test-area-7-share.md)
#### [테스트 영역 8: 플러그 인 전환](test-area-8-plug-in-switching.md)
## [소스 제어 VSPackage 만들기](creating-a-source-control-vspackage.md)
### [시작](getting-started-with-source-control-vspackages.md)
#### [소스 제어 VSPackage를 구현할지 여부 결정](determining-whether-to-implement-a-source-control-vspackage.md)
### [아키텍처](source-control-vspackage-architecture.md)
### [기능](source-control-vspackage-features.md)
#### [등록 및 선택 영역](registration-and-selection-source-control-vspackage.md)
#### [쿼리 편집 쿼리 저장](query-edit-query-save-source-control-vspackage.md)
#### [문자 모양 제어](glyph-control-source-control-vspackage.md)
#### [사용자 지정 사용자 인터페이스](custom-user-interface-source-control-vspackage.md)
### [디자인 요소](source-control-vspackage-design-elements.md)
#### [VSPackage 구조체](vspackage-structure-source-control-vspackage.md)
#### [관련 서비스 및 인터페이스](related-services-and-interfaces-source-control-vspackage.md)
#### [제공된 서비스](services-provided-source-control-vspackage.md)
# [마법사](wizards.md)
## [템플릿 디렉터리 설명(.Vsdir) 파일](template-directory-description-dot-vsdir-files.md)
## [마법사(.Vsz) 파일](wizard-dot-vsz-file.md)
## [마법사 인터페이스(IDTWizard)](wizard-interface-idtwizard.md)
## [컨텍스트 매개 변수](context-parameters.md)
## [사용자 지정 매개 변수](custom-parameters.md)
# [사용자 지정 도구](custom-tools.md)
## [단일 파일 생성기 구현](implementing-single-file-generators.md)
## [단일 파일 생성기 등록](registering-single-file-generators.md)
## [비주얼 디자이너에 형식 노출](exposing-types-to-visual-designers.md)
# [VSSDK 유틸리티](vssdk-utilities.md)
## [RegPkg 유틸리티](regpkg-utility.md)
### [RegPkg 패키지 등록 문제 해결](troubleshooting-regpkg-package-registration.md)
## [CreatePkgDef 유틸리티](createpkgdef-utility.md)
## [CreateExpInstance 유틸리티](createexpinstance-utility.md)
## [색 테마 도구](color-theming-tools.md)
### [VSIX 색 편집기](vsix-color-editor.md)
### [VSIX 색 컴파일러](vsix-color-compiler.md)
## [이미지 서비스 도구](image-service-tools.md)
### [리소스의 매니페스트](manifest-from-resources.md)
### [코드로의 매니페스트](manifest-to-code.md)
### [이미지 라이브러리 뷰어](image-library-viewer.md)
# [Windows Installer를 사용하여 VSPackage 설치](installing-vspackages-with-windows-installer.md)
## [Windows Installer 기본 사항](windows-installer-basics.md)
## [VSPackage 설치 시나리오](vspackage-setup-scenarios.md)
## [Windows Installer 패키지 작성](authoring-a-windows-installer-package.md)
## [시스템 요구 사항 검색](detecting-system-requirements.md)
## [구성 요소 관리](component-management.md)
## [VSPackage용 설치 디렉터리 선택](choosing-the-installation-directory-for-a-vspackage.md)
## [VSPackage 등록](vspackage-registration.md)
## [프로젝트 형식 배포](deploying-project-types.md)
## [방법: 설치 관리자의 레지스트리 정보 생성](how-to-generate-registry-information-for-an-installer.md)
## [설치 후 실행해야 하는 명령](commands-that-must-be-run-after-installation.md)
## [Windows Installer를 사용하여 VSPackage 제거](uninstalling-a-vspackage-with-windows-installer.md)
