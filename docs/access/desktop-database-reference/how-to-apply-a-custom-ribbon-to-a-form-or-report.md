---
título: aplicar una cinta de opciones personalizada a un formulario o informe TOCTitle: aplicar una cinta de opciones personalizada a un formulario o informe <<<<<<< HEAD ms:assetid: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: ms.date 48545865: 18/09/2015 === === Descripción: cómo aplicar cintas de opciones personalizadas al cargar un formulario o informe en Access 2013.
MS:AssetId: 7dcdfa42-3eaa-43f9-b99d-56b2cac97f84 ms:mtpsurl: https://msdn.microsoft.com/library/Ff196428(v=office.15) ms:contentKeyID: ms.date 48545865: 16/10/2018
>>>>>>> mtps_version principal: Office.15
---

# <a name="apply-a-custom-ribbon-to-a-form-or-report"></a>Aplicar una cinta de opciones personalizada a un formulario o informe

<<<<<<< HEAD

**Se aplica a**: Access 2013 | Office 2013

La cinta usa marcado XML declarativo basado en texto que simplifica su creación y personalización. Con unas pocas líneas de XML se puede crear la interfaz adecuada para el usuario. Access proporciona flexibilidad a la hora de personalizar la interfaz de usuario de la cinta. Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. En este tema se explica cómo aplicar cintas personalizadas al cargar un formulario o un informe.

## <a name="making-the-ribbon-customization-xml-available"></a>Activar la personalización de la cinta XML

**Almacenar la extensibilidad de la cinta XML en una tabla**

Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.

**USysRibbons** es una tabla del sistema creada por el usuario. La tabla se debe crear con nombres de columna específicos para que se implementen las personalizaciones de la cinta. La siguiente tabla muestra la configuración para usar al crear la tabla **USysRibbons**.
=======
**Se aplica a**: Access 2013 | Office 2013

La cinta usa el marcado XML declarativa basada en texto que simplifica la creación y personalización de la cinta. Con unas pocas líneas de XML se puede crear la interfaz adecuada para el usuario. Access proporciona flexibilidad a la hora de personalizar la interfaz de usuario de la cinta. 

Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. En este tema se explica cómo aplicar cintas personalizadas al cargar un formulario o un informe.

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
<<<<<<< HEAD
<td><p>Contiene el nombre de la cinta personalizada que se asociará a esta personalización.</p></td>
=======
<td><p>Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</p></td>
>>>>>>>patrón
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Memo</p></td>
<<<<<<< HEAD
<td><p>Contiene el XML de extensibilidad de cinta (RibbonX) que define la personalización de la cinta.</p></td>
=======
<td><p>Contiene el XML (RibbonX) que define la personalización de la cinta de opciones de extensibilidad de la cinta de opciones.</p></td>
>>>>>>>patrón
</tr>
</tbody>
</table>


<<<<<<< HEAD **cargar el código XML de extensibilidad de la cinta de opciones mediante programación**

Puede usar el método **[LoadCustomUI](https://msdn.microsoft.com/library/ff194416\(v=office.15\))** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.
=======
### <a name="load-ribbon-extensibility-xml-programmatically"></a>Cargar el código XML de extensibilidad de la cinta de opciones mediante programación

Puede usar el método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.
>>>>>>> master

El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.

Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, el método **LoadCustomUI** se ejecuta automáticamente y todas las cintas personalizadas estarán disponibles para la aplicación.

<<<<<<< HEAD
## <a name="assigning-custom-ribbons-to-forms-or-reports"></a>Asignar cintas personalizadas a formularios o informes
=======
## <a name="assign-custom-ribbons-to-forms-or-reports"></a>Asignar cintas de opciones personalizadas a formularios o informes
>>>>>>> master

1.  Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.

2.  Abra el formulario o informe en la vista Diseño.

<<<<<<< HEAD
3.  En la pestaña Diseño, haga clic en **Hoja de propiedades**.

4.  En la ficha **Todos** de la ventana Propiedad, haga clic en la lista **Nombre de banda de opciones** y, a continuación, seleccione una cinta.
=======
3.  En la ficha Diseño, elija **Hoja de propiedades**.

4.  En la ficha **todos** de la ventana Propiedades, elija la lista **Nombre de la cinta de opciones** y, a continuación, seleccione una cinta de opciones.
>>>>>>> master

5.  Guarde, cierre y vuelva a abrir el formulario o el informe. Se muestra la IU de la cinta que ha seleccionado.


> [!NOTE]
> Las fichas mostradas en la interfaz de usuario de la cinta de opciones son aditivos. Es decir, a menos que oculte las fichas específicamente o establezca el atributo *empezar desde el principio* en **True**, las fichas que se muestran en un formulario o interfaz de usuario de la cinta de opciones del informe son además de las fichas existentes.

> [!NOTE]
> [!NOTA] Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


