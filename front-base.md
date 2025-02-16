
- Vite의 HMR (Hot Module Replacement) 기능으로 빠른 개발 환경을 제공합니다.
- 기본 URL은 보통 [http://localhost:3000](http://localhost:3000) 입니다.

---

## 6. 빌드 및 배포

1. **프로덕션 빌드**
   - 아래 명령어로 어플리케이션을 빌드합니다.
     ```bash
     npm run build
     ```
   - 빌드 결과물은 `dist` 폴더에 생성됩니다.

2. **sitemap 생성**
   - 빌드 후 sitemap을 생성하려면 다음 명령어를 실행합니다.
     ```bash
     npm run gen-sitemap
     ```

3. **배포 스크립트**
   - `deploy.sh` 스크립트를 사용하여 Google Cloud Storage 등 원하는 플랫폼에 배포할 수 있습니다.
   - 배포 스크립트를 실행하기 전에 환경 변수나 프로젝트 ID 등의 설정을 확인하세요.

---

## 7. 커스터마이징 및 확장

- **다국어 설정 (i18n)**
  - `src/i18n/config.ts`와 `src/i18n/locales/` 폴더에서 번역 파일을 관리합니다.
  - 필요한 언어를 추가하거나 수정할 수 있습니다.
  
- **스타일링**
  - `Tailwind CSS`와 `Styled Components`를 혼용하여 사용하고 있으며, `src/styles/` 폴더에서 CSS 파일을 수정할 수 있습니다.
  - Vite 설정 파일에서 `publicDir` 옵션도 확인하세요.

- **컴포넌트 확장**
  - `src/components/` 폴더에 새로운 UI 컴포넌트를 추가하여 재사용성을 높입니다.
  - `@/` alias를 사용하여 경로 관리를 효율적으로 할 수 있습니다.

- **애니메이션 및 Web Worker**
  - `react-spring`을 활용한 애니메이션 효과와, `Web Worker`를 사용한 별 생성 로직 등 성능 최적화 기법을 적용해보세요.
  
- **배포 자동화**
  - 현재 배포 스크립트(deploy.sh)는 gsutil을 사용한 Google Cloud 배포 예시를 포함합니다.
  - 필요에 따라 CI/CD 파이프라인과 연동해 자동 배포를 구성할 수 있습니다.

---

## 8. 추가 자료 및 참고 링크

- [Vite 공식 문서](https://vitejs.dev/)
- [React 공식 문서](https://reactjs.org/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [Tailwind CSS 문서](https://tailwindcss.com/docs)
- [react-i18next 공식 문서](https://react.i18next.com/)

---

## 9. 마무리

이 가이드를 통해 현재 코드베이스를 활용하여 새로운 프론트엔드 어플리케이션 환경을 쉽게 구축할 수 있습니다. 필요에 따라 각 파일과 설정을 커스터마이징하여 여러분의 프로젝트에 맞게 확장해 나가세요.

즐거운 코딩 되세요!
