<template>
  <div class="text-center pa-4">
    <v-dialog v-model="taskStore.showDialogDelete" max-width="500" persistent>
      <v-card
        prepend-icon="mdi-delete"
        text="This action can't be reverted."
        title="Are you sure you want delete this task?"
      >
        <template v-slot:actions>
          <v-spacer></v-spacer>

          <v-btn @click="taskStore.toggleDelete()"
          color="red-darken-1"
          variant="elevated"> No </v-btn>

          <v-btn @click="taskStore.deleteTask()"
          color="red-darken-1"
          variant="outlined"> Yes </v-btn>
        </template>
      </v-card>
    </v-dialog>
  </div>
</template>

<script setup>
import { useTaskStore } from '@/stores/task.js';

const taskStore = useTaskStore();
</script>
