import { createStore } from "../redux";
import Todo from "./reducer/Todo";
import Counter from "./reducer/Counter";

let combineReducers = (reducers) =>
    (state={}, action) => {
        let newState = {};
        for( let r in reducers){
            newState[r] = reducers[r](state[r],action);
        }
        return newState;
    }
let store = createStore(combineReducers({Todo,Counter}));

export default store;