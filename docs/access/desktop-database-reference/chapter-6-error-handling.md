---
title: 'Capítulo 6: Control de errores'
TOCTitle: 'Chapter 6: Error Handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ec3a8972f8ca46754971eee7e8aa4a70c367a349
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868332"
---
# <a name="chapter-6-error-handling"></a>Capítulo 6: Control de errores


**Se aplica a**: Access 2013, Office 2013

ADO utiliza varios métodos diferentes para notificar a una aplicación los errores que se producen. En este capítulo, se explican los tipos de errores que se pueden producir cuando se trabaja con ADO y cómo se notifican a la aplicación. Se termina con unas sugerencias acerca de cómo tratar estos errores.

## <a name="how-does-ado-report-errors"></a>¿Cómo informa ADO de los errores?

ADO notifica los errores de varias formas:

  - Los errores de ADO generan un error en tiempo de ejecución. Trate un error de ADO de la misma manera que lo haría con cualquier otro error en tiempo de ejecución, por ejemplo, utilizando una instrucción **On Error** en Visual Basic.

  - Su programa puede recibir errores de OLE DB. Un error de OLE DB también genera un error en tiempo de ejecución.

  - Si el error es específico de su proveedor de datos, aparecen objetos **Error** en la colección **Errors** del objeto **Connection** que se utilizó para obtener acceso al almacén de datos cuando se produjo el error.

  - Si el proceso que desencadenó un evento también generó un error, la información de error se incluye en un objeto **Error** y se pasa como parámetro al evento. Vea el [Capítulo 7: Controlar eventos de ADO](chapter-7-handling-ado-events.md)para obtener más información acerca de eventos.

  - Los problemas que se producen al procesar actualizaciones por lotes o al ejecutar otras operaciones masivas que implican a un **conjunto de registros** pueden indicarse mediante la propiedad **Status** del **conjunto de registros**. Por ejemplo, infracciones de restricción de esquema o permisos no suficientes se pueden especificar mediante valores de **RecordStatusEnum**.

  - Los problemas que se producen implicando a un **campo** determinado del registro activo también se indican mediante la propiedad **Status** de cada **campo** de la colección **Fields** del **registro** o del **conjunto de registros**. Por ejemplo, actualizaciones que no se han podido completar o tipos de datos incompatibles se pueden especificar mediante valores de **FieldStatusEnum**.

En las secciones siguientes, se describe cada uno de estos métodos de notificación con más detalle.

- [Errores de ADO](ado-errors.md)

- [Referencia de Error ADO](ado-error-reference.md)

- [Errores de proveedor](provider-errors.md)

- [Información de errores relacionados con campos](field-related-error-information.md)

- [Información de errores relacionados con conjuntos de registros](recordset-related-error-information.md)

- [Anticipación de errores](anticipating-errors.md)

- [Handling Errors in Other Languages (ADO)](handling-errors-in-other-languages.md)