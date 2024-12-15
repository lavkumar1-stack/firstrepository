<persistence xmlns="http://xmlns.jcp.org/xml/ns/persistence"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/persistence
  http://xmlns.jcp.org/xml/ns/persistence/persistence_2_1.xsd"
	version="2.1">

	<persistence-unit name="lav">
		<provider>org.hibernate.jpa.HibernatePersistenceProvider</provider>
		<shared-cache-mode>ENABLE_SELECTIVE</shared-cache-mode>      <!-- for caching -->  
		<properties>
			<property name="javax.persistence.jdbc.driver"
				value="com.mysql.cj.jdbc.Driver" />
			<property name="javax.persistence.jdbc.url"
				value="jdbc:mysql://localhost:3306/DataBase_Name" />
			<property name="javax.persistence.jdbc.user"
				value="root" />
			<property name="javax.persistence.jdbc.password"
				value="lavkr005@mysql" />
			<property name="hibernate.show_sql" value="true" />
			<property name="hibernate.hbm2ddl.auto" value="update" />
			<property name="hibernate.dialect" value="org.hibernate.dialect.MySQL8Dialect"/>

<!-- for caching --> 
			<property name="hibernate.cache.use_second_level_cache" value="true"></property>
			<property name="hibernate.cache.region.factory_class" value="org.hibernate.cache.ehcache.EhCacheRegionFactory"></property>
  			
		</properties>
	</persistence-unit>
</persistence>
