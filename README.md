# BD MINI CHAT APP
## Login Interface
![Login Interface](./src/images/Chat%20app.PNG)

## Chat App Project Folder Structure
![Folder Structure](./src/images/Folder%20Structure.PNG)

### Frontend Setup

`HTML` Code
`CSS` Code


### Backend Setup

`JAVASCRIPT` Code
`Node Js` Code


## Main Package - Socket.io
### Admin & User Joining Code 
``` js
socket.on('join', (options, callback) => {
      const { error, user } = addUser({ id: socket.id, ...options })


      if (error) {
         return callback(error)
      }


        socket.join(user.room)

     socket.emit('message', generateMessage('Admin', 'Welcome!'))
     socket.broadcast.to(user.room).emit('message', generateMessage('Admin', `${user.username} has joined!`))
     io.to(user.room).emit('roomData', {
      room: user.room,
      users: getUsersInRoom(user.room)
     })

     callback()
     })

     ```

    ## Link
     Render Deployed Link https://bd-chat-app.onrender.com/ (BD CHAT APP)





