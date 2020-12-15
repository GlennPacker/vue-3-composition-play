<template>
  <div>
    <composition-refs />
    <reactive-composition />
    <composition-modular />
    <composition-first />
    <composition-second />
  </div>
</template>

<script>
import CompositionFirst from './CompositionFirst';
import CompositionModular from './CompositionModular';
import CompositionRefs from './CompositionRefs';
import ReactiveComposition from './ReactiveComposition';

import CompositionSecond from './CompositionSecond';

export default {
  name: 'HelloWorld',
  components: {
      CompositionRefs,
      CompositionFirst,
      CompositionModular,
      CompositionSecond,
      ReactiveComposition
  },
  props: {
    msg: String
  }
}
</script>
