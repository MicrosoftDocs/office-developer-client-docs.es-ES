---
título: aplicar una cinta de opciones personalizada al iniciar Access TOCTitle: aplicar una cinta de opciones personalizada al iniciar Access <<<<<<< HEAD ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: ms.date 48546659: 18/09 / 2015 === Descripción: cómo aplicar cintas de opciones personalizadas al abrir una base de datos en Access 2013. MS:AssetId: 9e8ddf95-35aa-4e57-8422-d770da14711e ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15) ms:contentKeyID: ms.date 48546659: 16/10/2018
>>>>>>> mtps_version principal: Office.15
---

# <a name="apply-a-custom-ribbon-when-starting-access"></a>Aplicar una cinta de opciones personalizada al iniciar Access

**Se aplica a:** Access 2013 | Office 2013

La cinta usa el marcado XML declarativa basada en texto que simplifica la creación y personalización de la cinta. Con unas pocas líneas de XML, puede crear la interfaz adecuada para el usuario. Access proporciona una gran flexibilidad para personalizar la interfaz de usuario de la cinta. Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. Este tema describe cómo aplicar cintas personalizadas al abrir una base de datos.

<<<<<<< HEAD
## <a name="making-the-ribbon-customization-xml-available"></a>Activar la personalización de la cinta XML

### <a name="storing-ribbon-extensibility-xml-in-a-table"></a>Almacenar la extensibilidad de la cinta XML en una tabla

Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.

**USysRibbons** es una tabla del sistema creada por el usuario. La tabla se debe crear con nombres de columna específicos para que se implementen las personalizaciones de la cinta. La siguiente tabla muestra la configuración para usar al crear la tabla **USysRibbons**.
=======
## <a name="make-the-ribbon-customization-xml-available"></a>Poner a disposición de la personalización de la cinta de opciones XML

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Almacenar código XML de extensibilidad de la cinta de opciones en una tabla

Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.

**USysRibbons** es una tabla del sistema creada por el usuario. La tabla debe crearse utilizando nombres de columna específicos para las personalizaciones de la cinta de opciones para se puedan implementar. 

La tabla siguiente describe la configuración que se utilizará al crear la tabla **USysRibbons**.
>>>>>>> master

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<<<<<<< HEAD
<th><p>Nombre de columna</p></th>
<th><p>Tipo de datos</p></th>
=======
<th><p>Nombre de columna</p></th>
<th><p>Tipo de datos</p></th>
>>>>>>>patrón
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Texto</p></td>
<td><p>Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memo</p></td>
<<<<<<< HEAD
<td><p>Contiene el código XML de extensibilidad de la Cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</p></td>
=======
<td><p>Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</p></td>
>>>>>>>patrón
</tr>
</tbody>
</table>


<<<<<<< HEAD
### <a name="loading-ribbon-extensibility-xml-programmatically"></a>Cargar XML de extensibilidad de cinta mediante programación

Puede usar el método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.

El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.

Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, el método **LoadCustomUI** se ejecuta automáticamente y todas las cintas personalizadas estarán disponibles para la aplicación.

## <a name="applying-customized-ribbons-when-access-starts"></a>Aplicar las cintas personalizadas al iniciar Access
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a>Cargar el código XML de extensibilidad de la cinta de opciones mediante programación

Puede usar el método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.

El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.

Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, se ejecuta automáticamente el método **LoadCustomUI** y todas las cintas de opciones personalizadas están disponibles para la aplicación.

## <a name="apply-customized-ribbons-when-access-starts"></a>Aplicar las cintas de opciones personalizadas al iniciar Access
>>>>>>> master

Para aplicar una interfaz de usuario personalizada para que esté disponible cuando se inicia la aplicación, use el siguiente procedimiento:

1.  Siga el proceso descrito anteriormente para que las cintas personalizadas estén disponibles para la aplicación.

2.  Cierre y reinicie la aplicación.

<<<<<<< HEAD
3.  Haga clic en el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, haga clic en **Opciones de Access**.

4.  Haga clic en la opción **Base de datos actual** y, en la sección **Opciones de la cinta y de la barra de herramientas**, haga clic en la lista **Nombre de la cinta** y seleccione una cinta.
=======
3.  Elija el **Botón de Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y, a continuación, elija **Opciones de Access**.

4.  Elija la opción de **Base de datos actual** y, a continuación, en la sección **Opciones de barra de herramientas y la cinta de opciones** , elija la lista **Nombre de la cinta de opciones** y seleccione una cinta de opciones.
>>>>>>> master

5.  Cierre y reinicie la aplicación. Se muestra la interfaz de usuario seleccionada.

> [!NOTE]
> [!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


