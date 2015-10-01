<메모만들기>

<div class="field">
    <%= f.label :memo %><br>
    <%= f.text_area :memo%>
   </div>
   
  _form.html.erb에 위에 것을 추가함
  
  
  views/contacts/show.html.erb에
  
  <p>
  <strong>Memo:</strong>
  <%= @contact.memo %>
</p> 
를 추가

controllers/contacts_controller.rb에 

def contact_params
      params.require(:contact).permit(:name, :phone_number, :memo)
    end
    
    :memo를 추가함
