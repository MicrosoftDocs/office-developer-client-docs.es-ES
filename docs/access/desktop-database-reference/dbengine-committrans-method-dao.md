---
title: Método DBEngine.CommitTrans (DAO)
TOCTitle: CommitTrans Method
ms:assetid: 0c9d345f-13ff-7fe6-789d-fbdb43fa54b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845171(v=office.15)
ms:contentKeyID: 48543197
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 75918ac4da32020214d9e58d866c5def169eede3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294390"
---
# <a name="dbenginecommittrans-method-dao"></a>Método DBEngine.CommitTrans (DAO)


**Se aplica a:** Access 2013, Office 2013

Termina la transacción actual y guarda los cambios.

## <a name="syntax"></a>Sintaxis

*expresión* . CommitTrans(***Option***)

*expression* Variable que representa un objeto **DBEngine**.

## <a name="parameters"></a>Parameters

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nombre</p></th>
<th><p>Obligatorio/opcional</p></th>
<th><p>Tipo de datos</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Opción</em></p></td>
<td><p>Opcional</p></td>
<td><p><strong>Long</strong></p></td>
<td><p>En un área de trabajo de Microsoft Access, puede incluir la constante <strong>dbForceOSFlush</strong> con <strong>CommitTrans</strong>. Esto fuerza al motor de base de datos a guardar de inmediato todas las actualizaciones en el disco, en lugar de guardarlas en la caché temporalmente. Si no utiliza esta opción, un usuario podría recuperar el control de inmediato después de que el programa de aplicación llame a <strong>CommitTrans</strong>, apagar el equipo y no haber escrito los datos en el disco. Aunque el uso de esta opción puede afectar al rendimiento de la aplicación, es útil en situaciones en las que el equipo puede apagarse antes de guardar en el disco las actualizaciones de la memoria caché.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Los métodos de transacción **BeginTrans**, **CommitTrans** y **Rollback** administran el procesamiento de transacciones durante una sesión definida por un objeto **Workspace**. Estos métodos se utilizan con un objeto **Workspace** cuando se desea tratar un conjunto de cambios realizados en las bases de datos en una sesión como una sola unidad.

Normalmente, se utilizan transacciones para mantener la integridad de los datos cuando es necesario actualizar registros en dos o más tablas y, al mismo tiempo, asegurarse de que los cambios se realizan (se validan) en todas las tablas o en ninguna (se revierten). Por ejemplo, si transfiere dinero de una cuenta a otra, podría restar una cantidad de una cuenta y agregar dicha cantidad a la otra cuenta. Si alguna de las actualizaciones no se realiza correctamente, las cuentas no cuadrarán. Utilice el método **BeginTrans** antes de actualizar el primer registro y, a continuación, si la siguiente actualización produce un error, puede utilizar el método **Rollback** para deshacer todas las actualizaciones. Use el método **CommitTrans** una vez actualizado correctamente el último registro.

> [!NOTE]
> [!NOTA] Dentro de un objeto **Workspace**, las transacciones son siempre globales con respecto al **Workspace** y no se limitan a un único objeto **Connection** o **Database**. Si realiza operaciones en varias conexiones o bases de datos dentro de una transacción de **Workspace**, la resolución de las transacciones (por ejemplo, mediante el método **CommitTrans** o **Rollback**) afecta a todas las operaciones en todas las conexiones y bases de datos dentro de esa área de trabajo.

Después de utilizar **CommitTrans**, no se pueden deshacer los cambios realizados a no ser que la transacción esté anidada dentro de otra transacción que haya sido revertida. Si anida transacciones, debe resolver la transacción actual antes de resolver una transacción situada en un nivel de anidamiento superior.

Si desea realizar transacciones simultáneas con ámbitos superpuestos no anidados, puede crear objetos **Workspace** adicionales que contengan las transacciones simultáneas.

Si cierra un objeto **Workspace** sin resolver las transacciones pendientes, las transacciones se revierten automáticamente.

Si utiliza el método **CommitTrans** o **Rollback** sin usar primero el método **BeginTrans**, se produce un error.

Es posible que algunas bases de datos ISAM usadas en un área de trabajo de Microsoft Access no admitan transacciones, en cuyo caso la propiedad **Transactions** del objeto **Database** o del objeto **Recordset** es **False**. Para asegurarse de que la base de datos admite transacciones, compruebe el valor de la propiedad **Transactions** del objeto **Database** antes de usar el método **BeginTrans**. Si usa un objeto **Recordset** basado en varias bases de datos, compruebe la propiedad **Transactions** del objeto **Recordset**. Si un objeto **Recordset** se basa íntegramente en tablas del motor de base de datos de Microsoft Access, siempre puede usar transacciones. No obstante, es posible que los objetos **Recordset** basados en tablas creadas por otros productos de base de datos no admitan transacciones. Por ejemplo, no puede usar transacciones en un objeto **Recordset** basado en una tabla de Paradox. En este caso, la propiedad **Transactions** es **False**. Si los objetos **Database** o **Recordset** no admiten transacciones, los métodos se omiten y no se produce ningún error.

No puede anidar transacciones si tiene acceso a orígenes de datos de ODBC a través del motor de base de datos de Microsoft Access.

En áreas de trabajo de ODBC, cuando usa **CommitTrans**, es posible que el cursor ya no sea válido. Use el método **Requery** para ver los cambios en **Recordset**, o bien cierre y vuelva a abrir **Recordset**.


> [!NOTE]
> - A menudo, es posible aumentar el rendimiento de la aplicación dividiendo las transacciones que requieren acceso al disco en bloques de transacciones. De esta forma, las operaciones se almacenan en un búfer y se reduce considerablemente el número de operaciones de acceso al disco.
> - En un área de trabajo de Microsoft Access, las transacciones se registran en un archivo almacenado en el directorio especificado por la variable de entorno TEMP en la estación de trabajo. Si el archivo de registro de transacciones utiliza todo el espacio de almacenamiento disponible en la unidad TEMP, el motor de base de datos genera un error en tiempo de ejecución. En este punto, si utiliza **CommitTrans**, se validan un número indeterminado de transacciones, pero las operaciones incompletas restantes se pierden y es necesario reiniciar la operación. Al utilizar el método **Rollback**, se libera el registro de transacciones y se revierten todas las operaciones de la transacción.
> - Al cerrar una copia del objeto **Recordset** en una transacción pendiente, se genera una operación **Rollback** implícita.


