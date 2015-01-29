proxy_redirect                  off;

proxy_set_header                Host            $host;
proxy_set_header                X-Real-IP       $remote_addr;
proxy_set_header                X-Forwarded-For $proxy_add_x_forwarded_for;

client_max_body_size            32m;
client_body_buffer_size         128k;

proxy_connect_timeout           5;
proxy_send_timeout              90;
proxy_read_timeout              90;

proxy_buffer_size               4k;
proxy_buffers                   4 32k;
proxy_busy_buffers_size         64k;
proxy_temp_file_write_size      64k;