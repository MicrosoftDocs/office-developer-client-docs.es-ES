---
title: Ocultar la cinta de opciones al iniciar Access
TOCTitle: Hide the ribbon when Access starts
description: Cómo cargar una cinta personalizada que oculte todas las fichas integradas en Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 4ce9327790f620ba9163f5cdbe7b5c8900de4341
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291946"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Ocultar la cinta de opciones al iniciar Access

**Se aplica a:** Access 2013, Office 2013

De manera predeterminada, Microsoft Access no dispone de un método para ocultar la cinta. En este tema se describe de qué manera se puede cargar una cinta personalizada que oculte todas las fichas integradas.

Para cargar la Cinta de opciones personalizada al iniciar Access, deberá almacenar su configuración en una tabla denominada **USysRibbons**.

La tabla **USysRibbons** deberá crearse utilizando nombres de columna específicos para que las personalizaciones de la Cinta de opciones se puedan implementar. 

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

<br/>

La tabla siguiente muestra la configuración de personalización de la cinta de opciones para almacenar en la tabla **USysRibbons**.

|Nombre de columna|Valor|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="https://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Aplicar una cinta de opciones personalizada al iniciar Access

Para implementar una interfaz de usuario personalizada con objeto de que esté disponible al iniciarse la aplicación, haga lo siguiente:

1.  Siga el proceso descrito previamente para poner la Cinta de opciones personalizada a disposición de la aplicación.

2.  Cierre la aplicación y, a continuación, reiníciela.

3.  Elija el **botón Microsoft Office**![O12FileMenuButton\_ZA10077102](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102") y luego elija **Opciones de Access**.

4.  Seleccione la opción **Base de datos activa** y, en la sección **Opciones de barra de herramientas y de la cinta de opciones**, haga clic en la lista **Nombre de cinta de opciones** y seleccione **HideTheRibbon**.

5.  Cierre y vuelva a iniciar la aplicación.

> [!NOTE]
> Para obtener más información sobre la interfaz de usuario de la cinta en otras aplicaciones de Office, consulte [Información general de la cinta de Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


