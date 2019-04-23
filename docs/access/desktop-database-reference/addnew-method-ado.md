---
title: AddNew (método, ADO)
TOCTitle: AddNew method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f733c574ba7927587c6fcb6305a361ca1070de0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282516"
---
# <a name="addnew-method-ado"></a>AddNew (método, ADO)

**Se aplica a:** Access 2013, Office 2013

Crea un nuevo registro de un objeto [Recordset](recordset-object-ado.md) actualizable.

## <a name="syntax"></a>Sintaxis

*objeto Recordset*. AddNew **, Values, *valores*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*recordset* |Un objeto **Recordset**.|
|*FieldList* |Es opcional. Un solo nombre o una matriz de nombres o posiciones ordinales de los campos en el nuevo registro.|
|*Values* |Opcional. Un solo valor o una matriz de valores para los campos en el registro nuevo. Si *Fieldlist* es una matriz, *Values* también debe ser una matriz con el mismo número de miembros; en caso contrario, se genera un error. El orden de los nombres de campo debe coincidir con el orden de los valores de campo en cada matriz.|

## <a name="remarks"></a>Comentarios

Use el método **AddNew** para crear e inicializar un registro nuevo. Utilice el método [Supports](supports-method-ado.md) con **adAddNew** (un valor de [CursorOptionEnum](cursoroptionenum.md)) para comprobar si puede agregar registros al actual objeto **Recordset**.

Tras llamar al método **AddNew**, el registro nuevo se convierte en el registro actual y permanece actual después de llamar al método [Update](update-method-ado.md). Dado que el registro nuevo se anexa al objeto **Recordset**, una llamada a **MoveNext** después de la llamada a Update hará que se realice un desplazamiento hasta más allá del final del objeto **Recordset**, por lo que el valor de **EOF** será True. Si el objeto **Recordset** no admite marcadores, es posible que no pueda obtener acceso al nuevo registro cuando se mueva a otro registro. Dependiendo del tipo de cursor, puede que tenga que llamar al método [Requery](requery-method-ado.md) para que el registro nuevo sea accesible.

Si llama a **AddNew** mientras modifica el registro actual o agrega un registro nuevo, ADO llamará al método **Update** para guardar todos los cambios y, después, ADO creará el registro nuevo.

El comportamiento del método **AddNew** depende del modo de actualización del objeto **Recordset** y de si se pasan los argumentos *Fieldlist* y *Values*.

En el *modo de actualización inmediata* (donde el proveedor escribe los cambios en el origen de datos subyacente cuando se llama al método **Update**), si llama al método **AddNew** sin argumentos, la propiedad [EditMode](editmode-property-ado.md) se establece en **adEditAdd** (un valor de [EditModeEnum](editmodeenum.md)). El proveedor almacena en la memoria caché local todos los cambios de los valores de campo. Si llama al método **Update**, se envía el nuevo registro a la base de datos y se restablece la propiedad **EditMode** en **adEditNone** (un valor de **EditModeEnum**). Si pasa los argumentos *Fieldlist* y *Values*, ADO envía inmediatamente el nuevo registro a la base de datos (no es necesario llamar a **Update**); el valor de la propiedad **EditMode** no cambia (**adEditNone**).

En el *modo de actualización por lotes* (donde el proveedor almacena varios cambios en la memoria caché y los escribe en el origen de datos subyacente sólo cuando se llama al método [UpdateBatch](updatebatch-method-ado.md)), si se llama al método **AddNew** sin argumentos, se establece el valor de la propiedad **EditMode** en **adEditAdd**. El proveedor almacena todos los cambios de los valores de campo en la memoria caché local. Si se llama al método **Update**, se agrega el nuevo registro al actual objeto **Recordset** y se restablece el valor de la propiedad **EditMode** en **adEditNone**, pero el proveedor no envía los cambios a la base de datos subyacente hasta que se llama al método **UpdateBatch**. Si pasa los argumentos *Fieldlist* y *Values*, ADO envía el nuevo registro al proveedor para que lo almacene en una memoria caché; es preciso llamar al método **UpdateBatch** para enviar el nuevo registro a la base de datos subyacente.

