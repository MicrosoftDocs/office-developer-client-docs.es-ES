---
title: EjecutarAplicación (acción de macro)
TOCTitle: RunApplication Macro Action
ms:assetid: 29967e6e-c441-b115-3ee6-2299b8a3bc25
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192038(v=office.15)
ms:contentKeyID: 48543885
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm93359
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bf7e64c3c60098bf95a101773dbbb678ea5b711f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879994"
---
# <a name="runapplication-macro-action"></a>EjecutarAplicación (acción de macro)


**Se aplica a**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Nota de seguridad" alt="Security note" />de seguridad**</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sea prudente al ejecutar archivos ejecutables o código en macros y aplicaciones. Los archivos ejecutables o el código se pueden usar para llevar a cabo acciones que podrían vulnerar la seguridad de su equipo y de los datos.</td>
</tr>
</tbody>
</table>


Puede usar la función **EjecutarAplicación** para ejecutar una aplicación basada en Microsoft Windows o MS-DOS, como Microsoft Excel, Microsoft Word o Microsoft PowerPoint, desde Microsoft Access. Por ejemplo, es posible que desee pegar datos de hoja de cálculo de Excel en la base de datos de Access.


> [!NOTE]
> <P>[!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.</P>



## <a name="setting"></a>Configuración

La acción **EjecutarAplicación** tiene el siguiente argumento.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Línea de comandos</strong></p></td>
<td><p>La línea de comandos que se utiliza para iniciar la aplicación (con la ruta de acceso y otros parámetros necesarios, tales como las opciones que ejecutan la aplicación de un modo particular). Introduzca la línea de comandos en el cuadro <strong>Línea de comandos</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Este argumento es obligatorio.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La aplicación seleccionada con esta acción se carga y se ejecuta en primer plano. La macro que contiene esta acción continúa su ejecución una vez iniciada la aplicación.

Puede transferir datos entre Access y la otra aplicación mediante el mecanismo de intercambio dinámico de datos (DDE) o el Portapapeles. Puede usar la acción **EnviarTeclas** para enviar pulsaciones de teclas a la otra aplicación (aunque DDE es un método más eficiente para transferir datos). También puede compartir datos entre aplicaciones mediante automatización.

Las aplicaciones basadas en MS-DOS se ejecutan en una ventana MS-DOS dentro del entorno de Windows.

En los sistemas operativos Windows, hay varias formas de ejecutar una aplicación: iniciar el programa desde el Explorador de Windows, utilizar el comando **Ejecutar** en el menú **Inicio** o hacer doble clic en el icono de un programa en el Escritorio de Windows.

La acción **EjecutarAplicación** no se puede ejecutar en un módulo de Visual Basic para Aplicaciones (VBA). En su lugar, utilice la función **Shell** de VBA.

