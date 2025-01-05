# GroupChat
MulticastSocket for Group Communication: The code uses MulticastSocket to enable group communication. This allows multiple clients to join a multicast group and send/receive messages to/from the group.

Thread for Reading Messages: A separate thread (ReadThread) is spawned to continuously read messages from the multicast group. This ensures that the main thread can handle user input while the ReadThread handles incoming messages.

Joining and Leaving the Group: The code includes logic for joining the multicast group using socket.joinGroup(group) and leaving the group using socket.leaveGroup(group). This ensures proper management of group membership.

Message Broadcasting: Messages are broadcasted to the group using DatagramPacket and MulticastSocket.send(). Each message is prefixed with the sender's name and a timestamp to provide context.

Handling User Input and Termination: The main thread handles user input and checks for the termination command ("Exit"). When a user types "Exit", the program notifies the group that the user has left, removes the user from the active users set, and closes the socket.
