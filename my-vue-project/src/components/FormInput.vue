import FormInput from './components/FormInput.vue';

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    HelloWorld,
    FormInput
  },
  setup() {
    const counter = useCounter();
    return { counter };
  }
}
