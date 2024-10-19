# Usage with Expo Router

First, create a custom layout adapter for the native bottom tabs:

```tsx
import { withLayoutContext } from "expo-router";
import { createNativeBottomTabNavigator } from "react-native-bottom-tabs/react-navigation";

export const Tabs = withLayoutContext(
  createNativeBottomTabNavigator().Navigator
);
```

Then, use the `Tabs` navigator in your app:

```tsx
import { Tabs } from "@/components/bottom-tabs";

export default function TabLayout() {
  return (
    <Tabs>
      <Tabs.Screen
        name="index"
        options={{
          title: "Home",
          tabBarIcon: () => ({ sfSymbol: "house" }),
        }}
      />
      <Tabs.Screen
        name="explore"
        options={{
          title: "Explore",
          tabBarIcon: () => ({ sfSymbol: "person" }),
        }}
      />
    </Tabs>
  );
}
```

For props and more information, see the [React Navigation integration guide](/docs/guides/usage-with-react-navigation).

Example: [EvanBacon/expo-router-react-native-bottom-tabs](https://github.com/EvanBacon/expo-router-react-native-bottom-tabs)
