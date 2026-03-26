---
marp: true
theme: default
header: "Headerタイトル"
style: |
  section {
    font-size: 28px;
    background-repeat: no-repeat /* 共通 */;
  }

  section:not(.cover) {
    background-image: url("../slide_template.svg");
    background-position: top left;
    background-size: 1280px;
  }

  section.cover {
    background-image: url("../cover_template.svg");
    background-position: center center;
    background-size: cover;
    /* color: white; */
  }

  h1 {
    font-size: 42px;
  }
  h2 {
    font-size: 36px;
  }
  img {
    max-height: 450px;
    display: block;
    margin: 0 auto;
  }
  a {
    color: #0066cc;
  }

---
<!-- _class: cover -->

# スライドタイトル

## サブタイトル

2026年3月26日

---

## Flutter Testing Overview
<!-- Flutterアプリケーションの品質を保証するためのテスト戦略 -->

### Why Testing Matters

- **Quality Assurance**: Ensures your app works as expected
- **Regression Prevention**: Catches bugs before they reach production
- **Confidence**: Refactor and add features without fear
- **Documentation**: Tests serve as living documentation

---

## Test Pyramid
<!-- テストピラミッド：効率的なテスト戦略 -->

![Test Pyramid](../image/001.png)

### Three Layers of Testing

1. **Unit Tests** (Base) - Fast, isolated, numerous
2. **Widget Tests** (Middle) - Component verification
3. **Integration Tests** (Top) - End-to-end scenarios

---

## Unit Tests
<!-- 単体テスト：ビジネスロジックの検証 -->

### Purpose
Test individual functions, methods, and classes in isolation

### Key Characteristics
- ✅ **Fast execution** (milliseconds per test)
- ✅ **No dependencies** on UI or external services
- ✅ **High coverage** goal (80%+ recommended)
- ✅ **Easy to debug** when failures occur

### Example Use Cases
```dart
// Testing business logic
test('calculate total price with discount', () {
  final calculator = PriceCalculator();
  expect(calculator.apply(100, 0.2), equals(80));
});
```

---

## Widget Tests
<!-- ウィジェットテスト：UIコンポーネントの検証 -->

### Purpose
Verify UI components render correctly and handle user interactions

### Key Characteristics
- 🎨 **UI verification** without running full app
- 🎨 **Interaction testing** (taps, scrolls, input)
- 🎨 **Layout validation** and visual regression
- 🎨 **Faster than integration** tests

### Example Test Scenarios
- Button displays correct text and responds to taps
- Form validation shows error messages
- List renders items from mock data
- Navigation triggers on user action

---

## Integration Tests
<!-- 統合テスト：エンドツーエンドのシナリオ検証 -->

### Purpose
Test complete user flows in a real device/simulator environment

### Key Characteristics
- 🚀 **Full app testing** with real interactions
- 🚀 **Device/Simulator** required for execution
- 🚀 **Critical paths** coverage (login, checkout, etc.)
- 🚀 **Slower execution** but highest confidence

### Example Scenarios
1. User registration flow (input → validation → API → success)
2. Purchase workflow (browse → cart → payment → confirmation)
3. Offline mode handling and sync

---

## Test Best Practices
<!-- テストのベストプラクティス -->

### Do's ✅
- **Write tests first** (TDD approach when possible)
- **Keep tests independent** - no shared state
- **Use descriptive names** - explain what and why
- **Mock external dependencies** - network, database, sensors
- **Test edge cases** - null, empty, extreme values

### Don'ts ❌
- **Don't test framework code** - trust Flutter SDK
- **Don't skip flaky tests** - fix or remove them
- **Don't over-mock** - test real behavior when safe
- **Don't ignore coverage** - aim for meaningful coverage

---

## Testing Tools & Packages
<!-- Flutter テストエコシステム -->

### Core Testing
- `flutter_test` - Built-in testing framework
- `test` - Dart test package (unit tests)
- `integration_test` - Official integration testing

### Popular Packages
- `mockito` / `mocktail` - Mocking dependencies
- `bloc_test` - Testing BLoC pattern
- `golden_toolkit` - Visual regression testing
- `patrol` - Enhanced integration testing

### CI/CD Integration
- Run tests on GitHub Actions, Bitrise, Codemagic
- Automated coverage reports (Codecov, Coveralls)

---

## Summary
<!-- まとめ：テストで開発を加速 -->

### Key Takeaways

1. **Test Pyramid** - Balance unit, widget, and integration tests
2. **Start Early** - Write tests alongside features, not after
3. **Automate** - Run tests in CI/CD pipeline
4. **Maintain** - Keep tests updated as code evolves

### Resources
- [Flutter Testing Docs](https://docs.flutter.dev/testing)
- [Effective Dart: Testing](https://dart.dev/guides/language/effective-dart)

**Happy Testing! 🎯**
