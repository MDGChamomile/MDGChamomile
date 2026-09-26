# 하네스 최소주의: 절차는 얇게, 경계는 단단하게

> “Every component in a harness encodes an assumption about what the model can't do on its own, and those assumptions are worth stress testing, both because they may be incorrect, and because they can quickly go stale as models improve.”
>
> — Anthropic, [Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)

> “Find the simplest solution possible, and only increase complexity when needed.”
>
> — Anthropic, [Building effective agents](https://www.anthropic.com/research/building-effective-agents)

- 과거 모델의 한계를 보완하기 위해 도입했던 복잡한 절차와 하네스가 성능이 향상된 최신 모델에서는 오히려 자율성과 효율을 저해할 수 있다. 모델이 별도의 개입 없이 안정적으로 수행 가능한 작업에 과도한 개입을 유지하면 비용과 디버깅 부담만 높아진다.

- 목표, 필수 맥락, 성공 기준과 안전·권한·데이터 보호 경계를 남긴 '최소 기준선'에서 출발한다. 그 밖의 절차는 대표 평가나 실제 작업에서 반복·재현된 실패를 개선할 때만 최소한으로 추가한다. 다만 실패 비용이 크거나 되돌리기 어려운 위험은 사고가 반복되기 전에도 근거 있는 시스템 통제로 예방한다.

- 검증되지 않은 해결 절차를 기본값으로 강제하지 않는다. 최소 기준선 안에서 구체적인 해결 경로는 모델의 판단에 맡기고, 작업별 맥락은 필요할 때만 보완한다.

- 세션마다 상시 주입하는 컨텍스트는 프로젝트 목적과 핵심 제약으로 최소화한다. 지시와 예시를 무작정 늘리기보다 도구와 데이터의 구조를 먼저 정리하고, 일회성 정보나 로그는 필요할 때만 불러오도록 설계한다.

- 테스트와 실행 결과처럼 모델이 스스로 작업 결과를 직접 확인할 수 있는 피드백 루프를 제공한다. 실패 비용이 크거나 되돌리기 어려운 행동은 프롬프트에만 의존하지 않고 최소 권한, 격리, 명시적 승인 등의 시스템 레벨에서 직접 통제한다.

- 측정 전 임시 절차가 필요하면 가설, 적용 범위, 예상 손익, 재검토 시점과 제거 기준을 기록하고, 그 결정을 검증된 결론처럼 표현하지 않는다.

- 하네스의 절차나 장치는 동일한 핵심 경계를 유지한 최소 기준선과 비교해, 득실을 종합하여 실익에 따라 도입하거나 유지한다. 임시 절차는 정해 둔 시점과 기준에 따라 재검토한다. 일상적인 운영 절차는 유연하게 수정하되, 핵심 경계를 변경할 때는 명확한 근거와 하네스 소유자의 승인을 거친다.
