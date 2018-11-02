---
title: CopiarArchivoDeBaseDeDatos (acción de macro)
TOCTitle: CopyDatabaseFile macro action
ms:assetid: e6320b55-946b-9efc-9b64-b86513801a37
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835963(v=office.15)
ms:contentKeyID: 48548373
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f2034bb4d8d1fbf3f1a0a37bf6adc7c8b8001bb
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925208"
---
# <a name="copydatabasefile-macro-action"></a>CopiarArchivoDeBaseDeDatos (acción de macro)


**Se aplica a**: Access 2013, Office 2013

La acción **CopiarArchivoDeBaseDeDatos** se puede usar para realizar una copia de la base de datos de Microsoft SQL Server 7.0 o posterior que está conectada al proyecto de Access. Access desasocia la base de datos actual y, a continuación, adjunta al servidor de destino. Para obtener más información acerca de cómo se desasocia y asocia una base de datos, vea la documentación de SQL Server.


> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. Si desea más información sobre la activación de macros, consulte los vínculos de la sección See Also de este artículo.



## <a name="setting"></a>Configuración

La acción **CopiarArchivoDeBaseDeDatos** tiene los siguientes argumentos.

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
<td><p><strong>Nombre de archivo de la base de datos</strong></p></td>
<td><p>El nombre del nuevo Archivo de datos maestro. La ruta predeterminada para el archivo es la ubicación actual del archivo de proyecto de Access (.adp).</p></td>
</tr>
<tr class="even">
<td><p><strong>Sobrescribir archivo existente</strong></p></td>
<td><p>Especifica si hay que reemplazar o no un archivo existente con el mismo nombre. Si se establece en <strong>Sí</strong> y el nombre del archivo ya existe, se sobrescribe el archivo. Si se establece en <strong>No</strong> y el nombre del archivo ya existe, no se sobrescribe el archivo y falla la acción. Si el archivo no existe aún, se ignora esta configuración. El valor predeterminado es <strong>Sí</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Desconectar todos los usuarios</strong></p></td>
<td><p>Especifica si Access debe obligar a los usuarios a salir de la base de datos. Si se establece en <strong>Sí</strong>, todos los usuarios que estén conectados a la base de datos se desconectan para que pueda realizarse la operación de copia de la base de datos. Si se establece en <strong>No</strong> y hay uno o más usuarios conectados a la base de datos, se produce un error en la operación de copia de la base de datos. El valor predeterminado es <strong>No</strong>. 

</p>

> [!WARNING]
> Desconectar usuarios de una base de datos sin una advertencia adecuada puede generar pérdida de datos.


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

La operación de copia se realiza de manera sincrónica, por lo que no se pueden realizar otras operaciones hasta que la copia de la base de datos haya finalizado.

La acción **CopiarArchivoDeBaseDeDatos** no solo copia datos, definiciones de datos y objetos de base de datos, sino también copia propiedades extendidas, como valores predeterminados, restricciones de texto y valores de búsqueda.

Requisitos para copiar una base de datos:

  - Debe desconectar todas las aplicaciones y los usuarios antes de copiar el archivo de la base de datos.

  - Todos los objetos y las vistas excepto el Panel de navegación deben cerrarse.

  - La base de datos actual no se debe replicar.

  - La base de datos del servidor de origen debe ser Microsoft SQL Server versión 7.0 o superior, o SQL Server 2000 Desktop Engine en un equipo local.

<!-- end list -->

  - La base de datos de SQL Server del servidor de origen debe ser una base de datos de un solo archivo.

  - Debe ser miembro del rol sysadmin tanto en el equipo SQL Server de origen como en el de destino.

Para ejecutar la acción **CopiarArchivoDeBaseDeDatos** en un módulo de Visual Basic para Aplicaciones, utilice el método **CopyDatabaseFile** del objeto **DoCmd**.

