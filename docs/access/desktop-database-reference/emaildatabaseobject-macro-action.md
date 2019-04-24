---
title: EnviarPorCorreoObjetoDeBaseDeDatos (acción de macro)
TOCTitle: EMailDatabaseObject macro action
ms:assetid: 7fd80596-5c08-dab9-5343-c0edc38a1af9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196469(v=office.15)
ms:contentKeyID: 48545915
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm24439
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 15cb7d6c422a9d7b0fae17ab649b6cfbc1b497a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293570"
---
# <a name="emaildatabaseobject-macro-action"></a>EnviarPorCorreoObjetoDeBaseDeDatos (acción de macro)

**Se aplica a:** Access 2013 | Office 2013

La acción **EnviarPorCorreoObjetoDeBaseDeDatos** se utiliza para incluir un objeto hoja de datos, formulario, informe, módulo o página de acceso a datos especificado de Microsoft Access en un mensaje de correo electrónico, desde donde se puede examinar y enviar.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="settings"></a>Settings

La acción **EnviarPorCorreoObjetoDeBaseDeDatos** utiliza los siguientes argumentos.

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
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>El tipo de objeto que se va a incluir en el mensaje de correo. Haga clic en <strong>Tabla</strong> (en el caso de una hoja de datos de tabla), <strong>Consulta</strong> (si es una hoja de datos de una consulta), <strong>Formulario</strong> (para un formulario u hoja de datos de un formulario), <strong>Informe</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. No es posible enviar una macro. Si desea incluir el objeto activo, seleccione su tipo con este argumento, pero deje en blanco el argumento <strong>Nombre del objeto</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del objeto</strong></p></td>
<td><p>El nombre del objeto que se va a incluir en el mensaje de correo. El cuadro <strong>Nombre del objeto</strong> muestra todos los objetos del tipo seleccionado mediante el argumento <strong>Tipo de objeto</strong> que existen en la base de datos. Si deja ambos argumentos ( <strong>Tipo de objeto</strong> y <strong>Nombre del objeto</strong> ) en blanco, Access envía a la aplicación de correo un mensaje sin ningún objeto de base de datos. Si ejecuta una macro que contiene la acción <strong>EMailDatabaseObject</strong> en una base de datos de biblioteca, Acceso busca el objeto con ese nombre primero en la base de datos de biblioteca y después en la base de datos actual.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Formato de resultados</strong></p></td>
<td><p>El tipo de formato que desea usar para el objeto incluido. La lista de formatos que puede seleccionar variará en función de lo que seleccione para el argumento <strong>tipo de objeto</strong> . Los formatos disponibles pueden <strong>incluir excel 97-excel 2003 libro (*. xls)</strong>, <strong>libro binario de Excel (*. xlsb)</strong>, <strong>libro de Excel (*. xlsx)</strong>, <strong>HTML (*. htm, *. html)</strong>, <strong>libro de Microsoft Excel 5.0/95 (*. xls)</strong>, <strong>formato PDF </strong>, <strong>Fomat de texto enriquecido (*. rtf)</strong>, <strong>archivos de texto (*. txt)</strong>o <strong>formato XPS (*. XPS)</strong>. en el cuadro <strong>formato de salida</strong> . Los módulos solo se pueden enviar en formato de texto. Las páginas de acceso a datos solo se pueden enviar en formato HTML. Si deja este argumento en blanco, Access le preguntará por el formato de los resultados.</p></td>
</tr>
<tr class="even">
<td><p><strong>Para</strong></p></td>
<td><p>The recipients of the message whose names you want to put on the <strong>To</strong> line in the mail message. If you leave this argument blank, Access prompts you for the recipients' names. Separate the recipients' names you specify in this argument (and in the <strong>Cc</strong> and <strong>Bcc</strong> arguments) with a semicolon (;) or with the list separator set on the <strong>Number</strong> tab of the <strong>Regional Settings Properties</strong> dialog box in Microsoft Windows <strong>Control Panel</strong>. If the mail application can't identify the recipients' names, the message isn't sent and an error occurs.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>CC</strong></p></td>
<td><p>Destinatarios del mensaje cuyos nombres desee indicar en la línea <strong>CC</strong> (&quot;copia&quot;carbón) del mensaje de correo. Si deja en blanco este argumento, la línea <strong>CC</strong> del mensaje de correo queda en blanco.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bcc</strong></p></td>
<td><p>Destinatarios del mensaje cuyos nombres desee indicar en la línea <strong>CCO</strong> (&quot;copia&quot;carbón oculta) del mensaje de correo. Si deja en blanco este argumento, la línea <strong>CCO</strong> del mensaje de correo queda en blanco.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Asunto</strong></p></td>
<td><p>Asunto al que se refiere el mensaje. Este texto aparecerá en la línea <strong>Asunto</strong> del mensaje. Si deja en blanco este argumento, la línea <strong>Asunto</strong> del mensaje de correo queda en blanco.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Texto del mensaje</strong></p></td>
<td><p>Cualquier texto que desee incluir en el mensaje además del objeto de base de datos. Este texto aparecerá en el cuerpo principal del mensaje, después del objeto. Si deja este argumento en blanco, no se incluirá ningún texto. Si ha dejado los argumentos <strong>Tipo de objeto</strong> y <strong>Nombre del objeto</strong> en blanco, puede utilizar este argumento para enviar un mensaje de correo sin ningún objeto de base de datos.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Modificar el mensaje</strong></p></td>
<td><p>Especifica si el mensaje se puede modificar o no antes de enviarlo. Si selecciona <strong>Sí</strong>, la aplicación de correo electrónico se iniciará automáticamente y el mensaje podrá ser modificado. Si selecciona <strong>No</strong>, el mensaje se enviará sin dar opción a modificarlo. El valor predeterminado es <strong>Sí</strong>.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Archivo de plantilla</strong></p></td>
<td><p>La ruta de acceso y el nombre de un archivo que se desea utilizar como plantilla para un archivo HTML. El archivo de plantilla es un archivo que contiene etiquetas HTML.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

El objeto incluido en el mensaje de correo se encuentra en el formato especificado. Al hacer doble clic sobre el objeto, éste se abrirá con el software correspondiente.

The following rules apply when you use the **EMailDatabaseObject** action to include a database object in a mail message:

- Puede enviar hojas de datos de tabla, consulta y formulario. En el objeto incluido, todos los campos de la hoja de datos tienen la misma apariencia que en Access, excepto los campos que contengan objetos OLE. Las columnas de estos campos se incluyen en el objeto, pero los campos están en blanco.

- Para un control dependiente de un campo Sí/No (botón de alternancia, botón de opción o casilla de verificación), el archivo de salida muestra el valor –1 (Sí) o 0 (No).

- Para un cuadro de texto dependiente de un campo Hipervínculo, el archivo de salida muestra el hipervínculo para todos los formatos de salida excepto texto MS-DOS (en este caso, el hipervínculo se muestra como texto normal).

- Si se envía un formulario en la vista Formulario, el objeto incluido siempre contiene la vista Hoja de datos del formulario.

- Si envía un informe, los únicos controles que se incluirán en el archivo serán cuadros de texto y (en algunos casos) etiquetas. El resto de los controles se omiten. Tampoco se incluye la información del encabezado y el pie de página. La única excepción a esto es que, al enviar un informe en formato Excel, se incluirá un cuadro de texto en un pie de grupo que contenga una expresión con la función **Suma**. El objeto no incluirá ningún otro control del encabezado o pie de página (ni ninguna función de agregado distinta de **Suma**).

- Los subinformes se incluyen en el objeto.

- Si se envía una hoja de datos, formulario o página de acceso a datos en formato HTML, se crea un archivo .html. Si se envía un informe en formato HTML, se crea un archivo .html para cada página del informe.

Para ejecutar la acción **EnviarPorCorreoObjetoDeBaseDeDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **SendObject** del objeto **DoCmd**.

### <a name="about-the-contributor"></a>Sobre el colaborador

**Vínculo proporcionado por** Luke Chung, [FMS, Inc.](https://www.fmsinc.com/), fundador y Presidente de FMS, Inc., un proveedor líder de soluciones de bases de datos personalizadas y herramientas de desarrollo.

- [Características y límites del uso del método EnviarObjeto para enviar correos](https://www.fmsinc.com/microsoftaccess/email/sendobject.html)





