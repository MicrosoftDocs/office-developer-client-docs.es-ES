---
<<<<<<< Título HEAD: uso de TOCTitle de objetos de datos ActiveX: ms:assetid mediante objetos de datos ActiveX: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: ms.date 48545279: 18/09/2015 === título: ActiveX de uso TOCTitle de objetos de datos: Descripción utilizar objetos de datos ActiveX: Microsoft Access proporciona tres objetos modelos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.
MS:AssetId: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: ms.date 48545279: 16/10/2018
>>>>>>> maestro mtps_version: Office.15 f1_keywords:
- vbaac10.chm5285627 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="using-activex-data-objects"></a>Utilizar objetos de datos ActiveX


**Se aplica a**: Access 2013 | Office 2013

<a name="microsoft-access-provides-three-object-models-to-use-in-the-creation-maintaining-and-managing-of-your-access-databases-and-their-related-data-by-using-visual-basic"></a>Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y administración de bases de datos de Access y de sus datos relacionados, mediante la utilización de Visual Basic.
=======
# <a name="use-activex-data-objects"></a>Usar objetos de datos ActiveX

**Se aplica a**: Access 2013 | Office 2013

Microsoft Access proporciona tres modelos de objetos para utilizarlos en la creación, mantenimiento y la administración de las bases de datos de Access y sus datos relacionados, mediante el uso de Visual Basic.
>>>>>>> master

## <a name="microsoft-activex-data-objects-ado"></a>Objetos de datos ActiveX de Microsoft (Microsoft ActiveX Data Objects, ADO)

ADO contiene los objetos necesarios para crear, mantener y eliminar registros en un origen de datos dado.

<<<<<<< HEAD
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX proporciona los objetos del lenguaje de definición de datos (Data Definition Language, DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.

**Microsoft Jet and Replication Objects 2,5 Library (JRO)**

<a name="since-ado-objects-were-designed-to-work-with-many-databases-in-addition-to-microsoft-jet-databases-functionality-specific-to-jet-was-broken-out-into-the-jro-library"></a>Puesto que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de bases de datos Microsoft Jet, las funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.
=======
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. DDL y seguridad (ADOX)

ADOX proporciona los objetos de lenguaje de definición de datos (DDL) necesarios para crear una nueva base de datos y los objetos que contiene además de los objetos necesarios para administrar la seguridad.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Biblioteca de Microsoft Jet y Replication Objects 2.5 (JRO)

Debido a que los objetos ADO fueron diseñados para trabajar con muchas bases de datos además de las bases de datos Microsoft Jet, funciones específicas de Jet se incluyeron como parte de la biblioteca JRO.
>>>>>>> master

En la tabla siguiente se muestran la funcionalidad que proporcionan los distintos modelos de objetos comparados con DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Característica</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
<<<<<<< HEAD (sólo de Microsoft Access)</p></th>
=== (Sólo para MDB)</p></th>
>>>>>>> master
</tr>
</thead>
<tbody>
<tr class="odd">
<<<<<<< HEAD
<td><p>Crear conjuntos de registros</p></td>
=======
<td><p>Crear conjuntos de registros.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar propiedades de inicio</p></td>
=======
<td><p>Editar propiedades de inicio.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Admitir ANSI92 SQL***</p></td>
=======
<td><p>Admitir ANSI92 SQL.* **</p></td>
>>>>>>>patrón
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Crear tablas</p></td>
=======
<td><p>Crear tablas.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Crear nueva base de datos</p></td>
=======
<td><p>Crear nueva base de datos.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar propiedades de tabla existente</p></td>
=======
<td><p>Editar propiedades de tabla existente.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Crear relaciones de tablas</p></td>
=======
<td><p>Crear relaciones de tabla.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar la configuración de seguridad</p></td>
=======
<td><p>Editar configuración de seguridad.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Compatibilidad con el atributo Compression para datos de columnas</p></td>
=======
<td><p>Compatibilidad con el atributo Compression para datos de la columna.</p></td>
>>>>>>>patrón
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar consultas o vistas SQL básicas almacenadas</p></td>
=======
<td><p>Editar almacenados, básica consultas o vistas SQL.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Crear consultas permanentes que son accesibles sólo mediante código.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Crear consultas accesibles por medio de la interfaz de usuario y código del contenedor de base de datos</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Compactar o codificar la base de datos</p></td>
=======
<td><p>Compactar o codificar la base de datos.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Actualizar la caché</p></td>
=======
<td><p>Actualizar la memoria caché.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Hacer replicable la base de datos</p></td>
=======
<td><p>¿Hacer replicable la base de datos.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Hacer réplicas de la base de datos</p></td>
=======
<td><p>Hacer réplicas de la base de datos.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Sincronizar réplicas</p></td>
=======
<td><p>Sincronizar réplicas.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar las propiedades de base de datos</p></td>
=======
<td><p>Editar propiedades de base de datos.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Crear propiedades personalizadas de base de datos</p></td>
=======
<td><p>Crear propiedades de base de datos personalizada.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Modificar propiedades de columna de tabla</p></td>
=======
<td><p>Editar propiedades de columna de tabla.</p></td>
>>>>>>>patrón
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Sólo disponible cuando se trabaja con bases de datos Microsoft Access. Las versiones futuras del proveedor SQL pueden proporcionar estas funciones en proyectos de Microsoft Access (.adp).

\*\* Sólo disponible cuando se trabaja con proyectos de Access.

<<<<<<< HEAD \* \* \* aunque el motor de base de datos de Access admite en parte ANSI 92 SQL no resulta aún totalmente compatible con ANSI92.

1Utiliza el objeto **Connection** para hacer referencia a la base de datos

2Utiliza el objeto **Catalog** para hacer referencia a la base de datos

3Utiliza el objeto **Replica** para hacer referencia a la base de datos

4Utiliza el objeto **JetEngine** para hacer referencia a la base de datos


> [!NOTE]
> <a name="punlike-dao-ado-and-adox-objects-can-perform-the-marked-actions-in-databases-other-then-jet-as-long-as-the-provider-for-those-databases-supports-that-actionp"></a><P>[!NOTA] A diferencia de DAO, los objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos diferentes de Jet, siempre que el proveedor de éstas admita esa acción.</P>
=======
\*\*\*Aunque el motor de base de datos de Access admite en parte ANSI 92 SQL, todavía no es totalmente compatible con ANSI92.

1 objeto usa **conexión** a base de datos de referencia.

Objeto usa **catálogo** 2 a base de datos de referencia.

Objeto usa **réplica** 3 a base de datos de referencia.

Objeto usa **JetEngine** 4 a base de datos de referencia.


> [!NOTE]
> A diferencia de DAO, objetos ADO y ADOX pueden realizar las acciones marcadas en bases de datos que no sean de Jet de siempre y cuando el proveedor para las bases de datos admite esa acción.
>>>>>>> master


