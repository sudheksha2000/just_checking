CC = g++

CFLAGS= -g

SRCDIR = src

OBJDIR = obj

SRCS = $(wildcard $(SRCDIR)/*.cpp)

OBJS = $(SRCS:$(SRCDIR)/%.cpp=$(OBJDIR)/%.o)

INCDIR = inc

EXEC = ticket_system

target : 
	$(CC) $(SRCDIR)/*.cpp -I$(INCDIR)

all : clean $(EXEC)


$(OBJDIR)/%.o: $(SRCDIR)/%.cpp
	$(CC) $(CFLAGS) -c -o $@ $< -I$(INCDIR) -g 
    
$(EXEC): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^ 
	
	
clean:
	rm -f $(OBJDIR)/*.o $(EXEC) $(output)
	
