---
title: Objeto Field (referencia de base de datos de escritorio de Access)
TOCTitle: The Field object
ms:assetid: 55531e04-d74f-6394-df64-1660e5d572ca
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249284(v=office.15)
ms:contentKeyID: 48544926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2cbd5752399e5a14f08b7eb944e3a028ba53f561
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314024"
---
# <a name="field-object"></a>Field (objeto)

**Se aplica a:** Access 2013, Office 2013

Cada objeto **Field** suele corresponder a una columna en una tabla de la base de datos. Sin embargo, un **campo** también puede representar un puntero a otro **conjunto de registros**, denominado capítulo. Las excepciones, como las columnas de capítulo, se tratarán más adelante en esta guía.

Utilice la propiedad **Valor** de objetos **Field** para establecer o devolver datos para el registro activo. Dependiendo de la funcionalidad que exponga el proveedor, es posible que algunas colecciones, métodos o propiedades de un objeto **Field** no estén disponibles.

Con las colecciones, los métodos y las propiedades de un objeto **Field**, puede hacer lo siguiente:

- Devolver el nombre de un campo usando la propiedad **Name**.

- Ver o cambiar los datos del campo utilizando la propiedad **Valor**. **Valor** es la propiedad predeterminada del objeto **Field**.

- Devolver las características básicas de un campo mediante las propiedades **Tipo**, **Precision** y **NumericScale**.

- Devolver el tamaño declarado de un campo mediante la propiedad **DefinedSize**.

- Devolver el tamaño real de los datos de un campo dado mediante la propiedad **ActualSize**.

- Determinar qué tipos de funcionalidad se admiten para un campo dado utilizando la propiedad **Attributes** y la colección **Properties**.

- Manipular los valores de campos que contienen datos de caracteres Long o binarios largos utilizando los métodos **AppendChunk** y **GetChunk**.

- Resolver discrepancias en valores de campo durante una actualización por lotes (si el proveedor admite actualizaciones por lotes) utilizando las propiedades **OriginalValue** y **UnderlyingValue**.

## <a name="describing-a-field"></a>Describir un campo

Los temas que siguen tratan sobre propiedades del objeto [Field](field-object-ado.md) que representan información que describe el propio objeto **Field** (es decir, metadatos acerca del campo). Esta información puede servir para determinar mucho sobre el esquema del **conjunto de registros**. Estas propiedades son **Tipo**, **DefinedSize** y **ActualSize**, **Name**, y **NumericScale** y **Precision**.

## <a name="discovering-the-data-type"></a>Descubrir el tipo de datos

La propiedad **Tipo** indica el tipo de datos del campo. Las constantes enumeradas de tipo de datos que admite ADO se describen en [DataTypeEnum](datatypeenum.md) en la *Referencia del programador de ADO*.

Para tipos numéricos de coma flotante como **adNumeric**, se puede obtener más información. La propiedad **NumericScale** indica cuántos dígitos a la derecha del separador decimal se utilizarán para representar valores para el **campo**. La propiedad **Precision** especifica el número máximo de dígitos utilizados para representar valores para el **campo**.

## <a name="determining-field-size"></a>Determinar el tamaño del campo

Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.

Utilice la propiedad **ActualSize** para devolver la longitud real del valor de un objeto **Field**. Para todos los campos, la propiedad **ActualSize** es de sólo lectura. Si ADO no puede determinar la longitud del valor del objeto **Field**, la propiedad **ActualSize** devuelve **adUnknown**.

Las propiedades **DefinedSize** y **ActualSize** tienen propósitos diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado de **adVarChar** y un valor de la propiedad **DefinedSize** de 50, que contiene un solo carácter. El valor de la propiedad **ActualSize** que devuelve es la longitud en bytes de ese único carácter.

## <a name="determining-field-contents"></a>Determinación del contenido de los campos

El identificador de la columna desde el origen de datos se representa mediante la propiedad **Name** del **campo**. La propiedad **Valor** del objeto **Field** devuelve o establece el contenido de datos reales del campo. Esta es la propiedad predeterminada.

Para cambiar los datos de un campo, establezca la propiedad **Valor** en un valor nuevo del tipo correcto. Su tipo de cursor debe admitir actualizaciones para cambiar el contenido de un campo. La validación de la base de datos no se hace aquí en modo de proceso por lotes, por lo que deberá comprobar si hay errores cuando llame a **UpdateBatch** en tal caso. Algunos proveedores también admiten las propiedades **UnderlyingValue** y **OriginalValue** del objeto **Field** de ADO para ayudarle a resolver conflictos cuando intenta realizar actualizaciones por lotes. Para obtener detalles acerca de cómo resolver tales conflictos, vea el [Capítulo 4: Modificar datos](chapter-4-editing-data.md).

> [!NOTE]
> [!NOTA] Los valores del **campo Recordset** no se pueden establecer al anexar nuevos **campos** a un **conjunto de registros**. Más bien, los **campos** nuevos se pueden anexar a un **conjunto de registros** cerrado. Después, se debe abrir el **conjunto de registros**, y sólo entonces se podrán asignar valores a estos **campos**.

## <a name="getting-more-field-information"></a>Obtener más información sobre el campo

Los objetos de ADO tienen dos tipos de propiedades: integradas y dinámicas. Hasta ahora, se han descrito sólo las propiedades integradas del objeto **Field**.

Las propiedades integradas son aquellas propiedades implementadas en ADO y disponibles inmediatamente para cualquier objeto nuevo, mediante la sintaxis. No aparecen como objetos **Property** en la colección **Properties** de un objeto.

Las propiedades dinámicas las define el proveedor de datos subyacente, y aparecen en la colección **Properties** para el objeto de ADO apropiado. Por ejemplo, una propiedad específica del proveedor puede indicar si un objeto **Recordset** admite transacciones o actualizaciones. Estas propiedades adicionales aparecerán como objetos **Property** en la colección **Properties** de ese objeto **Recordset**. Sólo se puede hacer referencia a las propiedades dinámicas a través de la colección, utilizando la sintaxis Object. Properties (0) u or Object. Properties ("Name").

No se puede eliminar ningún tipo de propiedad.

Un objeto dinámico **Property** tiene cuatro propiedades integradas propias:

- La propiedad **Name** es una cadena que identifica la propiedad.

- La propiedad **Type** es un entero que especifica el tipo de datos de la propiedad.

- La propiedad **Value** es una variante que contiene la configuración de la propiedad. **Valor** es la propiedad predeterminada de un objeto **Property**.

- La propiedad **Attributes** es un valor **Long** que indica características de la propiedad específicas del proveedor.

La colección **Properties** del objeto **Field** contiene metadatos adicionales acerca del campo. El contenido de esta colección varía dependiendo del proveedor. El código de ejemplo siguiente examina la colección **Properties** del **conjunto de registros** de ejemplo que se presentó al principio de este capítulo. Primero examina el contenido de la colección. Este código utiliza [OLE DB Provider para SQL Server](microsoft-ole-db-provider-for-sql-server.md), de forma que la colección **Properties** contiene información relativa a ese proveedor.

```vb 
 
'BeginFieldProps 
 Dim objProp As ADODB.Property 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 
 For Each objProp In objFields(intLoop).Properties 
 Debug.Print vbTab & objProp.Name & " = " & objProp.Value 
 Next objProp 
 Next intLoop 
'EndFieldProps 
```

## <a name="dealing-with-binary-data"></a>Tratamiento de datos binarios

Utilice el método [AppendChunk](appendchunk-method-ado.md) en un objeto **Field** para rellenarlo con datos binarios largos o de caracteres. En situaciones en las que la memoria del sistema es limitada, puede utilizar el método **AppendChunk** para manipular valores largos por partes y no en su totalidad.

Si el bit **adFldLong** de la propiedad **Attributes** de un objeto **Field** está establecido en **True**, se puede usar el método **AppendChunk** para ese campo.

La primera llamada a **AppendChunk** en un objeto **Field** escribe datos en el campo y sobrescribe los que hubiese previamente. Después, las llamadas a **AppendChunk** se agregan a los datos existentes. Si está adjuntando datos a un campo y luego establece o lee el valor de otro campo en el registro activo, ADO supone que terminó de adjuntar datos al primer campo, Si llama al método **AppendChunk** en el primer campo otra vez, ADO interpreta la llamada como una operación **AppendChunk** nueva y sobrescribe los datos existentes. El acceso a campos en otros objetos **Recordset** que no son clones del primer objeto **Recordset** no interrumpe las operaciones **AppendChunk**.

Utilice el método **GetChunk** en un objeto **Field** para recuperar todos o parte de sus datos binarios largos o de caracteres. En situaciones en las que la memoria del sistema es limitada, puede utilizar el método **GetChunk** para manipular valores largos por partes y no en su totalidad.

Los datos devueltos por una llamada a **GetChunk** se asignan a *variable*. Si el valor de *Size* es mayor que el de los datos restantes, el método **GetChunk** devuelve sólo los datos restantes sin rellenar *variable* con espacios en blanco. Si el campo está vacío, el método **GetChunk** devuelve un valor nulo.

Cada llamada posterior a **GetChunk** recuperar datos a partir de donde terminó la llamada a **GetChunk** anterior. No obstante, si está recuperando datos de un campo y luego establece o lee el valor de otro campo en el registro activo, ADO supone que terminó de recuperar datos del primer campo. Si llama al método **GetChunk** en el primer campo otra vez, ADO interpreta la llamada como una operación **GetChunk** nueva y empieza a leer desde el principio de los datos. El acceso a campos en otros objetos **Recordset** que no son clones del primer objeto **Recordset** no interrumpe las operaciones **GetChunk**.

Si el bit **adFldLong** de la propiedad **Attributes** de un objeto **Field** está establecido en **True**, se puede usar el método **GetChunk** para ese campo.

Si no hay ningún registro activo cuando utiliza el método **GetChunk** o **AppendChunk** en un objeto **Field**, se produce el error 3021 (no hay registros activos).

Para obtener un ejemplo del uso de estos métodos para manipular datos binarios, vea los ejemplos [método AppendChunk](appendchunk-method-ado.md) y [método GetChunk](getchunk-method-ado.md) en la *Referencia del programador de ADO*.

