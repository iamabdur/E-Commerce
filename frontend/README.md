# frontend package structure
1. axios
2. react-helmet-async
3. redux=>state management
4. react-redux
5. reduct-thunk => to make the delay of the action
6. devtools-extension  => to monitor the state and changes
7. react-router-dom => load the component based on url value
# version
   "react-toastify": "^9.1.1",
   "redux": "^4.2.0",
    "redux-devtools-extension": "^2.13.9",
    "redux-thunk": "^2.4.2",
    "react": "^18.2.0",
    "react-bootstrap": "^1.6.6",
    "react-dom": "^18.2.0",
    "react-helmet-async": "^1.3.0",
    "react-js-pagination": "^3.0.3",
    "react-redux": "^8.0.5",
    "react-router-dom": "^6.6.1", 


# connectivity for react redux 
1. store.js => state management {configureStore as reduxjs/toolkit}
     import { combineReducers, configureStore } from "@reduxjs/toolkit";
     import thunk from "redux-thunk";
     import productsReducer from "./slices/productsSlice";
    import productReducer from './slices/productSlice';
    import authReducer from './slices/authSlice';
  import cartReducer from './slices/cartSlice';
   import orderReducer from './slices/orderSlice';
   import userReducer from './slices/userSlice'


const reducer = combineReducers({
    productsState: productsReducer,
    productState: productReducer ,
    authState: authReducer,
    cartState: cartReducer,
    orderState: orderReducer,
    userState: userReducer
})


const store = configureStore({
    reducer,
    middleware: [thunk]
})

export default store;


2. make the store in the store js in index.js
import store
 import provder from react-redux;
 <Provider store={store}>
      <App />
    </Provider>

3. create slice.js which is used for all the silces contains in the store,js


   