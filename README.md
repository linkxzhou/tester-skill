# tester-skill

An agent skill that treats tests as **proof**, not decoration. It routes testing work through four gates: TDD red→green, verification-before-claim, fake-test audit / retention, and test-slice review. Use it when reviewing or writing tests, hunting tautological / fake-green suites, doing TDD, verifying before claiming done, or deciding which tests to keep.

一个 Agent 技能：把测试当作**证据**而不是装饰。通过四道闸编排测试工作：红绿强制（TDD）、完成前验证、打假测 / 留删、测切片评审。适用于审查或编写测试、怀疑假绿、TDD、声称完成前的验证、测试缺口与 mutation、Agent 生成测试的打假、以及决定删留测试。

## Gates / 四道闸

| Gate | Sub-skill | One-liner |
|------|-----------|-----------|
| 1. Red→green | `subskills/tdd-red-green/` | RED before GREEN; minimal impl; tiny cleanup only |
| 2. Verify before claim | `subskills/verification-before-claim/` | No fresh command output this turn → cannot claim pass |
| 3. Audit / retention | `subskills/test-audit/` | Reject junk; keep/delete by retention bar |
| 4. Test-slice review | `subskills/review-tests/` | Structure, gaps, pyramid; hand off to code review |

References: `references/iron-laws.md`, `fake-test-patterns.md`, `good-test-writing.md`.

This package intentionally omits Playwright / browser E2E tooling.

## Install / 安装

```bash
npx skills add linkxzhou/tester-skill
```

Or clone:

```bash
git clone --depth 1 https://github.com/linkxzhou/tester-skill.git ~/.claude/skills/tester-skill
```

- GitHub: https://github.com/linkxzhou/tester-skill
- ClawHub: https://clawhub.ai/linkxzhou/tester-skill
- SkillHub: https://skillhub.cn/skills/user_16e7431e/tester-skill

## License

MIT
