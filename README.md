# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

<% @post_images.each do |post_image| %>
<div>
  <%= link_to post_image_path(post_image.id) do %>
    <%= image_tag post_image.get_image %>
  <% end %>
  <p>投稿ユーザー画像：<%= image_tag post_image.user.get_profile_image(100,100) %></p>
  <p>ショップ名：<%= post_image.shop_name %></p>
  <p>説明：<%= post_image.caption %></p>
  <p>ユーザーネーム：<%= post_image.user.name %></p>
  <p><%= link_to "#{post_image.post_comments.count} コメント", post_image_path(post_image.id) %></p>
</div>
<% end %>

<% @post_images.each do |post_image| %>
<div>
  <%= link_to post_image_path(post_image.id) do %>
    <%= image_tag post_image.get_image %>
  <% end %>
  <p>投稿ユーザー画像：<%= image_tag post_image.user.get_profile_image(100,100) %></p>
  <p>ショップ名：<%= post_image.shop_name %></p>
  <p>説明：<%= post_image.caption %></p>
  <p>ユーザーネーム：<%= post_image.user.name %></p>
  <p><%= link_to "#{post_image.post_comments.count} コメント", post_image_path(post_image.id) %></p>
</div>
<% end %>