<template>
  <v-form v-model="valid">
      <v-row>
				<v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-mail"
            required
          ></v-text-field>
        </v-col>

        <v-col
          cols="12"
          md="4"
        >
          <v-text-field
            v-model="password"
            :rules="passwordRules"
            :counter="10"
            label="Password"
            required
          ></v-text-field>
        </v-col>

      </v-row>
		<v-btn
			class="btn-login"
			color="green"
			type="submit"
			elevation="2"
			to="/home"
		>Login</v-btn>
	</v-form>
</template>

<script>
  export default {
    data: () => ({
      valid: false,
      firstname: '',
      password: '',
      passwordRules: [
        v => !!v || 'Password is required',
        v => v.length <= 10 || 'Password must be less than 10 characters',
      ],
      email: '',
      emailRules: [
        v => !!v || 'E-mail is required',
        v => /.+@.+/.test(v) || 'E-mail must be valid',
      ],
    }),
  }
</script>

<style scoped>
	.btn-login {
		color: white;
	}

</style>