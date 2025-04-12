<template>
    <div class="tasks_container">
        <div class="tasks-header">
            <input 
            v-model="newTask"
            type="text"
            placeholder="Enter a task"
            class="task-input"
            @keyup.enter="createTask"
            />
            <button @click="createTask" class="add-button">+</button>
        </div>
        
        <div class="tasks-list">
            <div
            v-for="task in tasks"
            :keys="task.id"
            class="task-item"
            >
                <div class="task-next">
                    {{ task.title }}
                </div>
                <button
                class="complete-button"
                @click="completeTask(task.id)">Done
            </button>
        </div>
        </div>
    </div>
</template>