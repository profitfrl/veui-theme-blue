<template>
    <article class="number-input-demo">
        <h1><code>&lt;veui-number-input&gt;</code></h1>
        <veui-form>
            <h2>风格</h2>
            <div class="options-desc">
                可选的风格 <span class="bg-gray-show">ui</span> 
                属性值： <span class="bg-gray-show">normal / strong</span>
            </div>
            <section>
                <veui-field
                    label="normal"
                >
                    <veui-number-input
                        v-model="number"
                        ui="normal"
                    >
                        <template slot="before">
                            Value
                        </template>
                    </veui-number-input>
                </veui-field>
                <veui-field
                    label="strong"
                >
                    <veui-number-input
                        v-model="number"
                        ui="strong"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                </veui-field>
            </section>
            <h2>尺寸</h2>
            <div class="options-desc">
                可选的尺寸 <span class="bg-gray-show">ui</span> 
                属性值： <span class="bg-gray-show">xs / s / m</span>
            </div>
            <section>
                <veui-field
                    label="xs"
                >
                    <veui-number-input
                        v-model="number"
                        ui="xs"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                    <veui-number-input
                        v-model="number"
                        ui="xs strong"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                </veui-field>
                <veui-field
                    label="s"
                >
                    <veui-number-input
                        v-model="number"
                        ui="s"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                    <veui-number-input
                        v-model="number"
                        ui="s strong"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                </veui-field>
                <veui-field
                    label="m"
                >
                    <veui-number-input
                        v-model="number"
                        ui="m"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                    <veui-number-input
                        v-model="number"
                        ui="m strong"
                    >
                        <template slot="before">
                            Value:
                        </template>
                    </veui-number-input>
                </veui-field>
            </section>
            <section>
                <h2>状态</h2>
                <veui-form>
                    <veui-field label="Readonly">
                        <veui-number-input
                            v-model="number7"
                            readonly
                        />
                        <veui-number-input
                            v-model="number8"
                            ui="strong"
                            readonly
                        />
                    </veui-field>
                    <veui-field
                        label="Disabled"
                        disabled
                    >
                        <veui-number-input v-model="number7"/>
                        <veui-number-input
                            ui="strong"
                            v-model="number7"/>
                    </veui-field>
                    <veui-field label="Invalid">
                        <veui-number-input
                            v-model="number7"
                            invalid
                        />
                        <veui-number-input
                            v-model="number8"
                            ui="strong"
                            invalid
                        />
                    </veui-field>
                </veui-form>
            </section>
        </veui-form>
    </article>
</template>

<script>
import {NumberInput, Field, Form} from 'veui';

export default {
    name: 'number-input',
    components: {
        'veui-number-input': NumberInput,
        'veui-field': Field,
        'veui-form': Form
    },
    data() {
        return {
            number: null,
            number1: null,
            number2: null,
            number3: null,
            number4: null,
            number5: null,
            number6: null,
            number7: 1024,
            number8: 2333
        };
    },
    methods: {
        handlePriceChange(val) {
            this.number7 = val;
        }
    }
};
</script>

<style lang="less">
.number-input-demo {
    .veui-form {
        .veui-field {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
            .veui-number-input {
                margin-right: 20px;
            }
        }
        .veui-form-label {
            width: 130px;
            color: #999;
        }
    }
    .sdf {
        margin-top: 60px;
    }
}

</style>
