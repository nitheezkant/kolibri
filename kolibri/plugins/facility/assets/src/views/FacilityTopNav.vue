<template>

  <Navbar>
    <NavbarLink
      :title="coreString('classesLabel')"
      :link="facilityPageLinks.ManageClassPage"
    >
      <KIcon
        icon="classes"
        :color="$themeTokens.textInverted"
        style="top: 0; width: 24px; height: 24px;"
      />
    </NavbarLink>
    <NavbarLink
      :title="coreString('usersLabel')"
      :link="facilityPageLinks.UserPage"
    >
      <KIcon
        icon="people"
        :color="$themeTokens.textInverted"
        style="top: 0; width: 24px; height: 24px;"
      />
    </NavbarLink>
    <NavbarLink
      :title="$tr('settings')"
      :link="facilityPageLinks.FacilitiesConfigPage"
    >
      <KIcon
        icon="settings"
        :color="$themeTokens.textInverted"
        style="top: 0; width: 24px; height: 24px;"
      />
    </NavbarLink>
    <NavbarLink
      :title="$tr('data')"
      :link="facilityPageLinks.DataPage"
    >
      <KIcon
        icon="save"
        :color="$themeTokens.textInverted"
        style="top: 0; width: 24px; height: 24px;"
      />
    </NavbarLink>
  </Navbar>

</template>


<script>

  import { mapGetters } from 'vuex';
  import Navbar from 'kolibri.coreVue.components.Navbar';
  import NavbarLink from 'kolibri.coreVue.components.NavbarLink';
  import commonCoreStrings from 'kolibri.coreVue.mixins.commonCoreStrings';

  export default {
    name: 'FacilityTopNav',
    components: {
      Navbar,
      NavbarLink,
    },
    mixins: [commonCoreStrings],
    computed: {
      ...mapGetters(['facilityPageLinks']),
    },
    $trs: {
      data: {
        message: 'Data',
        context: "Title of tab in 'Facility' section.",
      },
      settings: {
        message: 'Settings',
        context: "Title of tab in 'Facility' section.",
      },
    },
  };

</script>


<style lang="scss" scoped></style>
