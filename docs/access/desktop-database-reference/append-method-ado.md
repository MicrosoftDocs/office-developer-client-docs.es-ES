---
title: Append (método, ADO)
TOCTitle: Append method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a85faf900860dabb809a10a92985559b7a7cf2ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706082"
---
# <a name="append-method-ado"></a>Append (método, ADO)

**Se aplica a**: Access 2013, Office 2013

Anexa un objeto a una colección. Si la colección es [Fields](fields-collection-ado.md), se puede crear un nuevo objeto [Field](field-object-ado.md) antes de anexarlo a la colección.

## <a name="syntax"></a>Sintaxis

*colección*. Anexar *objeto*

*los campos*. Anexe el *nombre*, *tipo*, *DefinedSize*, *Attrib*, *FieldValue*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*collection* |Objeto de colección.|
|*fields* |Colección **Fields**.|
|*object* |Variable de objeto que representa el objeto que se va a anexar.|
|*Name* |Valor de tipo **String** que contiene el nombre del nuevo objeto **Field**. No puede ser el nombre de ningún objeto de *fields*.|
|*Type* |Valor de [DataTypeEnum](datatypeenum.md), cuyo valor predeterminado es **adEmpty**, que especifica el tipo de datos del nuevo campo. ADO no admite los siguientes tipos de datos, por lo que no deben usarse al anexar nuevos campos a un objeto **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.|
|*DefinedSize* |Es opcional. Un valor de tipo **Long** que representa el tamaño definido, en caracteres o bytes, del nuevo campo. El valor predeterminado de este parámetro se deriva de *Type*. Campos cuyo valor de DefinedSize es mayor que 255 bytes y campos tratados como columnas de longitud variable. (No se especifica el valor predeterminado de *DefinedSize*.)|
|*Attrib* |Es opcional. Un valor de [FieldAttributeEnum](fieldattributeenum.md), cuyo valor predeterminado es **adFldDefault**, que especifica los atributos del nuevo campo. Si no se especifica este valor, el campo contendrá atributos derivados de *Type*.|
|*FieldValue* |Es opcional. **Variant** que representa el valor del nuevo campo. Si no se especifica, el campo se anexa con un valor null.|

## <a name="remarks"></a>Comentarios

### <a name="parameters-collection"></a>Parameters (colección)

Es preciso establecer el valor de la propiedad [Type](type-property-ado.md) de un objeto [Parameter](parameter-object-ado.md) antes de anexarlo a la colección **Parameters**. Si selecciona un tipo de datos de longitud variable, también deberá establecer la propiedad [Size](size-property-ado.md) en un valor mayor que cero.

Describir personalmente los parámetros minimiza el número de llamadas al proveedor y, en consecuencia, mejora el rendimiento a la hora de usar procedimientos almacenados o consultas parametrizadas. Sin embargo, es preciso conocer las propiedades de los parámetros asociados a la consulta parametrizada o al procedimiento almacenado al que desee llamar.

Utilice el método [CreateParameter](createparameter-method-ado.md) para crear objetos **Parameter** con los valores de propiedad adecuados y utilice el método **Append** para anexarlos a la colección [Parameters](parameters-collection-ado.md). Esto le permite establecer y devolver los valores de parámetro sin tener que llamar al proveedor para obtener la información de los parámetros. Si escribe a un proveedor que no proporcione información de parámetros, debe utilizar este método para rellenar manualmente la colección **Parameters** y poder utilizar parámetros.

### <a name="fields-collection"></a>Fields (colección)

El parámetro *FieldValue* sólo es válido cuando se agrega un objeto **Field** a un objeto [Record](record-object-ado.md) , no a un objeto **Recordset** . Con un objeto **Record**, se pueden anexar campos y proporcionar valores al mismo tiempo. Con un objeto **Recordset**, se deben crear los campos mientras está cerrado el objeto **Recordset**, después abrir el objeto **Recordset** y asignar valores a los campos.


> [!NOTE]
> [!NOTA] Para los nuevos objetos **Field** que se han anexado a la colección **Fields** de un objeto **Record**, se debe establecer primero la propiedad [Value](value-property-ado.md) para que se puedan especificar las demás propiedades de **Field**. Primero, se debe asignar un valor específico a la propiedad **Value** y se debe llamar a [Update](update-method-ado.md) en la colección **Fields**. A continuación, se podrá obtener acceso a otras propiedades como [Type](type-property-ado.md) o [Attributes](attributes-property-ado.md).


Los objetos **Field** de los siguientes tipos de datos (**DataTypeEnum**) no se pueden anexar a la colección **Fields**; si se anexan, se generará un error: **adArray**, **adChapter**, **adEmpty**, **adPropVariant** y **adUserDefined**. Además, ADO no admite los siguientes tipos de datos: **adIDispatch**, **adIUnknown** y **adIVariant**. En el caso de estos tipos, no se producirá un error cuando se anexen, pero su uso puede generar resultados imprevisibles, incluidas pérdidas de memoria.

### <a name="recordset"></a>Recordset

Si no se establece la propiedad [CursorLocation](cursorlocation-property-ado.md) antes de llamar al método **Append**, el valor de **CursorLocation** se establecerá automáticamente en **adUseClient** (un valor de [CursorLocationEnum](cursorlocationenum.md)) cuando se llame al método [Open](recordset-object-ado.md) del objeto [Recordset](open-method-ado-recordset.md).

Se producirá un error en tiempo de ejecución si se llama al método **Append** en la colección **Fields** de un objeto **Recordset** abierto o en un objeto **Recordset** donde se ha configurado la propiedad [ActiveConnection](activeconnection-property-ado.md). Sólo se pueden anexar campos a un objeto **Recordset** que no está abierto y aún no se ha conectado a ningún origen de datos. Este suele ser el caso cuando se crea un objeto **Recordset** con el método [CreateRecordset](createrecordset-method-rds.md) o cuando se asigna a una variable de objeto.

### <a name="record"></a>Record

No se producirá un error en tiempo de ejecución si se llama al método **Append** en la colección **Fields** de un objeto **Record** abierto. El nuevo campo se agregará a la colección **Fields** del objeto **Record**. Si el objeto **Record** se deriva de un objeto **Recordset**, el nuevo campo no aparecerá en la colección **Fields** del objeto **Recordset**.

Se puede crear un campo inexistente y anexarlo a la colección **Fields** mediante la asignación de un valor al objeto de campo como si ya existiese en la colección. La asignación hará que se cree y se anexe automáticamente el objeto **Field** y, a continuación, se completa la asignación.

Después de anexar un objeto **Field** a la colección **Fields** de un objeto **Record**, llame al método **Update** de la colección **Fields** para guardar el cambio.

