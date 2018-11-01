---
title: ImportarExportarDatos (acción de macro)
TOCTitle: ImportExportData Macro Action
ms:assetid: 2cbde873-8a3d-b15c-4aab-405cddf44cea
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192107(v=office.15)
ms:contentKeyID: 48543961
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm51789
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 62a496867852afb89d5b556f6be793f3f8c3739e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887785"
---
# <a name="importexportdata-macro-action"></a>ImportarExportarDatos (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **ImportarExportarDatos** se utiliza para importar o exportar datos entre la base de datos de Access (.mdb o .accdb) o el proyecto de Access (.adp) actual y otra base de datos. Para bases de datos de Microsoft Access, también se puede vincular una tabla a la base de datos actual de Access desde otra base de datos. Con una tabla vinculada, se tiene acceso a los datos de la tabla mientras la propia tabla permanece en la otra base de datos.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.

## <a name="settings"></a>Configuración

La acción **ImportarExportarDatos** utiliza los siguientes argumentos.

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
<td><p><strong>Tipo de transferencia</strong></p></td>
<td><p>El tipo de transferencia que se desea realizar. Seleccione <strong>Importar</strong>, <strong>Exportar</strong> o <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. La opción predeterminada es <strong>Importar</strong>.  </p>

> [!NOTE]
> Los proyectos de Access (.adp) no admiten el tipo de transferencia **Vincular**.


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de base de datos</strong></p></td>
<td><p>El tipo de base de datos que se va a importar, exportar o vincular. Puede seleccionar <strong>Microsoft Access</strong> o alguno de los demás tipos de bases de datos del cuadro <strong>Tipo de base de datos</strong>. La opción predeterminada es <strong>Microsoft Access</strong>.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Nombre de la base de datos</strong></p></td>
<td><p>El nombre de la base de datos desde la que realizar la importación, la exportación o la vinculación. Este argumento es necesario. Para los tipos de base de datos que usan archivos separados para cada tabla, como FoxPro, Paradox y dBASE, escriba el directorio que contiene el archivo. Escriba el nombre del archivo en el argumento <strong>Origen</strong> (importar o vincular) o el argumento <strong>Destino</strong> (exportar). Para las bases de datos de ODBC, escriba la cadena de conexión de conectividad abierta de bases de datos (ODBC) completa.  </p>
<p>Para ver un ejemplo de una cadena de conexión, vincule una tabla externa a Access:</p>
<ol>
<li><p>En el cuadro de diálogo <strong>Obtener datos externos</strong>, escriba la ruta de acceso de la base de datos origen en el cuadro <strong>Nombre de archivo</strong>.</p></li>
<li><p>Haga clic en <strong>Vincular al origen de datos creando una tabla vinculada</strong> y luego en <strong>Aceptar</strong>.</p></li>
<li><p>Seleccione una tabla en el cuadro de diálogo <strong>Vincular tablas </strong> y haga clic en <strong> Aceptar </strong>.</p></li>
</ol>
<p>Abra la tabla recién vinculada en la vista Diseño y examine las propiedades de la tabla; para ello, haga clic en <strong>Hoja de propiedades</strong>, en la ficha <strong>Diseño</strong>, <strong>Herramientas</strong>. El texto de la propiedad <strong>Descripción</strong> es la cadena de conexión para esta tabla.  </p>
<p>Para obtener más información acerca de las cadenas de conexión ODBC, consulte el archivo de Ayuda u otra documentación para el controlador ODBC de este tipo de base de datos ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tipo de objeto</strong></p></td>
<td><p>El tipo del objeto que se va a importar o exportar. Si selecciona <strong>Microsoft Access</strong> para el argumento <strong>Tipo de base de datos</strong>, puede seleccionar <strong>Tabla</strong>, <strong>Consulta</strong>, <strong>Formulario</strong>, <strong>Informe</strong>, <strong>Macro</strong>, <strong>Módulo</strong>, <strong>Página de acceso a datos</strong>, <strong>Vista de servidor</strong>, <strong>Diagrama</strong>, <strong>Procedimiento almacenado</strong> o <strong>Función</strong> en el cuadro <strong>Tipo de objeto</strong>. La opción predeterminada es <strong>Tabla</strong>. Si selecciona cualquier otro tipo de base de datos o elige <strong>Vincular</strong> en el cuadro <strong>Tipo de transferencia</strong>, este argumento no se tiene en cuenta. Si está exportando una consulta de selección a una base de datos de Acces, seleccione <strong>Tabla</strong> en este argumento para exportar el conjunto de resultados de la consulta y seleccione <strong>Consulta</strong> para exportar la consulta en sí. Si está exportando una consulta de selección a otro tipo de base de datos, este argumento no se tiene en cuenta y el conjunto de resultados de la consulta se exporta.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Origen</strong></p></td>
<td><p>El nombre de la tabla, consulta de selección u objeto de Access que se desea importar, exportar o vincular. Para algunos tipos de bases de datos, tales como FoxPro, Paradox o dBASE, se trata de un nombre de archivo. Incluya la extensión del nombre de archivo (tal como .dbf) en el nombre del archivo. Este argumento es obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Destino</strong></p></td>
<td><p>El nombre de la tabla importada, exportada o vinculada, la consulta de selección o el objeto de Access de la base de datos de destino. Para algunos tipos de base de datos, como FoxPro, Paradox o dBASE, se trata de un nombre de archivo. Incluya la extensión del nombre de archivo (como .dbf) en el nombre de archivo. Es un argumento obligatorio. Si selecciona <strong>Importar</strong> en el argumento <strong>Tipo de transferencia</strong> y <strong>Tabla</strong> en el argumento <strong>Tipo de objeto</strong>, Access crea una nueva tabla que contiene los datos de la tabla importada. Si importa una tabla u otro objeto, Access agrega un número al nombre si está en conflicto con un nombre existente. Por ejemplo, si importa Empleados y ya existe, Access cambiará el nombre de la tabla o el otro objeto importado a Empleados1. Si exporta una base de datos de Access u otra base de datos, Access reemplazará automáticamente las tablas o los otros objetos existentes que tengan el mismo nombre.  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Estructura solamente</strong></p></td>
<td><p>Especifica si se debe importar o exportar sólo la estructura de una tabla de base de datos sin ninguno de sus datos. Seleccione <strong>Sí</strong> o <strong>No</strong>. La opción predeterminada es <strong>No</strong>.  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Puede importar y exportar tablas entre Access y otros tipos de bases de datos. También puede exportar consultas de selección de Access a otros tipos de bases de datos. Access exporta el conjunto de resultados de la consulta en forma de tabla. Puede importar y exportar cualquier objeto de base de datos de Access si ambas bases de datos son bases de datos de Access.

Si importa una tabla de otra base de datos de Access (.mdb o .accdb) que esté vinculada en esa base de datos, seguirá vinculada después de que la importe. Es decir, se importa el vínculo, no la propia tabla.

Si la base de datos a la que desea obtener acceso requiere una contraseña, aparecerá un cuadro de diálogo cuando ejecute la macro. Escriba la contraseña en ese cuadro de diálogo.

La acción **ImportarExportarDatos** es similar a los comandos de la ficha **Datos externos**, en **Importar** o **Exportar**. Estos comandos se utilizan para seleccionar un origen de datos como, por ejemplo, una base de datos de Access u otro tipo, una hoja de cálculo o un archivo de texto. Si selecciona una base de datos, aparecerán uno o más cuadros de diálogo en los que podrá seleccionar el tipo de objeto que desea importar o exportar (para bases de datos de Access), el nombre del objeto y otras opciones, según la base de datos de la que vaya a importar o a la que vaya a exportar o vincular. Los argumentos de la acción **ImportarExportarDatos** reflejan las opciones de estos cuadros de diálogo.

Si desea suministrar información de índices para una tabla vinculada de dBASE, primero vincule la tabla:

1.  Haga clic en **Archivo dBASE**.

2.  En el cuadro de diálogo **Obtener datos externos**, escriba la ruta de acceso del archivo de dBASE en el cuadro **Nombre de archivo**.

3.  Haga clic en **Vincular al origen de datos creando una tabla vinculada** y, a continuación, haga clic en **Aceptar**.

4.  Especifique los índices en los cuadros de diálogo para este comando. Access almacena la información de los índices en un archivo de información especial (.inf), ubicado en la carpeta de Microsoft Office.

5.  Luego, puede eliminar el vínculo a la tabla vinculada.

La siguiente vez que utilice la acción **ImportarExportarDatos** para vincular esta tabla de dBASE, Access usará la información de índice especificada.

> [!NOTE]
> [!NOTA] Si consulta o filtra una tabla vinculada, la consulta o el filtro distinguen entre mayúsculas y minúsculas.

Para ejecutar la acción **ImportarExportarDatos** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferDatabase** del objeto **DoCmd**.

