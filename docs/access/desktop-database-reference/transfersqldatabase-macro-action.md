---
title: TransferirBaseDeDatosSQL (acción de macro)
TOCTitle: TransferSQLDatabase macro action
ms:assetid: 8cb95e22-f1f0-6c70-7dcb-3a3e9aafdc57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197344(v=office.15)
ms:contentKeyID: 48546244
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm111536
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5ed20555726d0a6f63f0e48fb154cedb411ef8cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306849"
---
# <a name="transfersqldatabase-macro-action"></a>TransferirBaseDeDatosSQL (acción de macro)

**Se aplica a:** Access 2013, Office 2013

En un proyecto de Access, se puede utilizar la acción **TransferirBaseDeDatosSQL** para transferir una base de datos de Microsoft SQL Server 7.0 o posterior a otra base de datos de SQL Server 7.0 o posterior. Para obtener más información acerca de la transferencia de una base de datos, vea la documentación de SQL Server.

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza.

## <a name="setting"></a>Configuración

La acción **TransferirBaseDeDatosSQL** utiliza los siguientes argumentos.

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
<td><p><strong>Servidor</strong></p></td>
<td><p>El nombre de la base de datos de SQL Server 7.0 o posterior donde se están copiando los datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>Base de datos</strong></p></td>
<td><p>El nombre de la nueva base de datos que se creará en el servidor de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Usar conexión de confianza</strong></p></td>
<td><p>Especifica si existe o no una conexión de confianza con SQL Server. Si presenta el valor <strong>Sí</strong>, entonces existe una conexión de confianza y no se necesitan los argumentos <strong>Inicio de sesión</strong> y <strong>Contraseña</strong>. Si tiene el valor <strong>No</strong>, entonces es necesario especificar también los argumentos <strong>Inicio de sesión</strong> y <strong>Contraseña</strong>. La opción predeterminada es <strong>Sí</strong>. Cuando se usa una conexión de confianza, la seguridad de SQL Server se integra con la seguridad del sistema operativo Windows para proporcionar un único inicio de sesión en la red y en la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sesión</strong></p></td>
<td><p>El nombre de inicio de sesión en el servidor de destino.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>La contraseña para el argumento <strong>Inicio de sesión</strong>. Esta contraseña se almacena como texto en el proyecto de Access, pero se oculta durante la operación de transferencia de la base de datos.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transferir datos de copia</strong></p></td>
<td><p>Especifica si se deben incluir datos en la operación de transferencia de la base de datos. El valor <strong>Sí</strong> indica que se incluyen todos los datos en todas las tablas, junto con todas las estructuras de datos, propiedades extendidas y objetos de base de datos. La opción <strong>No</strong> indica que no se incluyen los datos en las tablas. En el servidor de destino sólo se crean la estructura de la tabla y las propiedades extendidas, junto con todos los objetos de base de datos (excepto diagramas de base de datos). La opción predeterminada es <strong>Sí</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

No es posible realizar otras operaciones mientras se transfiere la base de datos.

La acción **TransferirBaseDeDatosSQL** copia de forma predeterminada datos, definiciones de datos, objetos de base de datos y propiedades extendidas (tales como valores predeterminados, restricciones de texto y valores de búsqueda).

Existen ciertos requisitos para transferir una base de datos:

- El usuario debe ser un administrador del sistema en el servidor de destino (esto no es necesario en el servidor de origen).

- El servidor SQL Server conectado actualmente al proyecto de Access y el servidor de destino al que se está transfiriendo la base de datos debe ser SQL Server versión 7.0 o posterior.

  > [!NOTE]
  > Los servidores vinculados no se transfieren durante una operación de transferencia de base de datos.

Para ejecutar la acción **TransferirBaseDeDatosSQL** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **TransferSQLDatabase** del objeto **DoCmd**.

