---
title: Aplicar una cinta de opciones personalizada al iniciar Access
TOCTitle: Apply a custom ribbon when starting Access
description: Cómo aplicar las cintas de opciones personalizadas al abrir una base de datos en Access 2013.
ms:assetid: 9e8ddf95-35aa-4e57-8422-d770da14711e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198313(v=office.15)
ms:contentKeyID: 48546659
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 0acd99a498a74f098b08814e9f11d49b28bae097
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291960"
---
# <a name="apply-a-custom-ribbon-when-starting-access"></a>Aplicar una cinta de opciones personalizada al iniciar Access

**Se aplica a:** Access 2013, Office 2013

La cinta usa el marcado XML declarativa basada en texto que simplifica la creación y personalización de la cinta. Con unas pocas líneas de XML, puede crear la interfaz adecuada para el usuario. Access proporciona una gran flexibilidad para personalizar la interfaz de usuario de la cinta. Por ejemplo, el marcado de personalización se puede almacenar en una tabla, insertar en un procedimiento de VBA, almacenar en otra base de datos de Access o vincular desde una hoja de cálculo de Excel. Este tema describe cómo aplicar cintas personalizadas al abrir una base de datos.

## <a name="make-the-ribbon-customization-xml-available"></a>Activar la personalización de la cinta XML

### <a name="store-ribbon-extensibility-xml-in-a-table"></a>Almacenar la extensibilidad de la cinta XML en una tabla

Un método que puede usar para que las personalizaciones de la cinta estén disponibles es almacenarlas en una tabla. Si las almacena en una tabla denominada **USysRibbons**, las personalizaciones se pueden implementar sin usar macros o código VBA.

**USysRibbons** es una tabla de sistema creada por el usuario. La tabla se debe crear con nombres de columna específicos para que se implementen las personalizaciones de la cinta. 

La tabla siguiente muestra la configuración para crear la tabla **USysRibbons**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre de columna</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Text</p></td>
<td><p>Contiene el nombre de la Cinta de opciones personalizada que se asociará a esta personalización.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Notas</p></td>
<td><p>Contiene el código XML de extensibilidad de la cinta de opciones (RibbonX) que define la personalización de la Cinta de opciones.</p></td>
</tr>
</tbody>
</table>


### <a name="load-ribbon-extensibility-xml-programmatically"></a>Cargar XML de extensibilidad de cinta mediante programación

Puede usar el método **[LoadCustomUI](https://docs.microsoft.com/office/vba/api/Access.Application.LoadCustomUI)** para cargar las personalizaciones de la cinta mediante programación. Normalmente, para crear y hacer que la cinta esté disponible para la aplicación, primero debe crear un módulo en la base de datos con un procedimiento que llame al método **LoadCustomUI**, pasando el nombre de la cinta y el marcado de personalización XML.

El marcado de personalización XML puede venir de un objeto **Recordset** creado desde una tabla, desde un origen externo a la base de datos como un archivo XML que debe analizar en una cadena, o desde un marcado XML insertado directamente en el procedimiento. Puede crear varias cintas con varias llamadas al método **LoadCustomUI**, pasando un marcado XML diferente siempre que el nombre de cada cinta y el atributo **id** de las pestañas que conforman la cinta sean únicas.

Una vez completado el procedimiento, cree una macro AutoExec que llame al procedimiento con la acción RunCode. De este modo, cuando se inicia la aplicación, el método **LoadCustomUI** se ejecuta automáticamente y todas las cintas personalizadas estarán disponibles para la aplicación.

## <a name="apply-customized-ribbons-when-access-starts"></a>Aplicar cintas de opciones personalizadas al iniciar Access

Para aplicar una interfaz de usuario personalizada para que esté disponible cuando se inicia la aplicación, use el siguiente procedimiento:

1.  Siga el proceso descrito anteriormente para que las cintas personalizadas estén disponibles para la aplicación.

2.  Cierre y reinicie la aplicación.

3.  Elija el **botón Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y luego elija **Opciones de Access**.

4.  Haga clic en la opción **Base de datos actual** y, en la sección **Opciones de la cinta y de la barra de herramientas**, haga clic en la lista **Nombre de la cinta** y seleccione una cinta.

5.  Cierre y reinicie la aplicación. Se muestra la interfaz de usuario seleccionada.

> [!NOTE]
> Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


