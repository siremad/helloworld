<?xml version="1.0" encoding="UTF-8"?>
<!--
 ~ Hibernate Search, full-text search for your domain model
 ~
 ~ License: GNU Lesser General Public License (LGPL), version 2.1 or later
 ~ See the lgpl.txt file in the root directory or <http://www.gnu.org/licenses/lgpl-2.1.html>.
  -->
<!DOCTYPE hibernate-configuration PUBLIC
  "-//Hibernate/Hibernate Configuration DTD//EN"
  "http://www.hibernate.org/dtd/hibernate-configuration-3.0.dtd">

<hibernate-configuration>
    <session-factory>

        <property name="connection.driver_class">com.microsoft.sqlserver.jdbc.SQLServerDriver</property>
        <property name="connection.url">jdbc:sqlserver://OMEGA\MYSQL2019;databaseName=member;</property>
        <property name="connection.username">sa</property>
        <property name="connection.password"></property>

        <!-- JDBC connection pool (use the built-in) -->
        <property name="connection.pool_size">1</property>

        <!-- SQL dialect -->
        <property name="dialect">org.hibernate.dialect.SQLServerDialect</property>

        <!-- Enable Hibernate's automatic session context management -->
        <property name="current_session_context_class">thread</property>

        <!-- Disable the second-level cache  -->
        <property name="cache.provider_class">org.hibernate.cache.NoCacheProvider</property>

        <!-- Echo all executed SQL to stdout -->
        <property name="show_sql">true</property>

        <!-- Drop and re-create the database schema on startup -->
        <property name="hbm2ddl.auto">update</property>

        <property name="hibernate.search.default.directory_provider">filesystem</property>
        <property name="hibernate.search.default.indexBase">target/indexes</property>
       <!--   <mapping class="org.hibernate.search.test.spatial.POI"/>-->
        <mapping class="member"/>

    </session-factory>
</hibernate-configuration>
