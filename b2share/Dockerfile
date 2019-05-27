FROM eudatb2share/b2share:2.1.2

# Create non privileged user and chown 
# B2SHARE install folder and instance folder
# (By default files are stored in instance folder)
RUN adduser --uid 1000 invenio --gid 0 && \
    mkdir -p /usr/var/b2share-instance/files && \
    chown 1000:0 -R /usr/var/b2share-instance && \
    chown 1000:0 -R /eudat
 
USER 1000:0

CMD ["/eudat/b2share.sh"]
