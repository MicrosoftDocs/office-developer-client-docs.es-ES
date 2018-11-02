---
title: Guardar método - ActiveX Data Objects (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d779fc5cff955ca669635ca827456dafb8927d8a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919685"
---
# <a name="save-method-ado"></a>Save (método, ADO)


**Se aplica a**: Access 2013, Office 2013

Guarda el objeto [Recordset](recordset-object-ado.md) en un archivo o un objeto [Stream](stream-object-ado.md).

## <a name="syntax"></a>Sintaxis

*conjunto de registros*. Guardar*destino*, *PersistFormat*

## <a name="parameters"></a>Parámetros

  - *Destination*

  - Es opcional. **Variant** que representa la ruta de acceso completa al archivo donde se va a guardar el objeto **Recordset** o una referencia a un objeto **Stream**.

  - *PersistFormat*

  - Es opcional. Valor de [PersistFormatEnum](persistformatenum.md) que especifica el formato en el que se va a guardar el objeto **Recordset** (XML o ADTG). El valor predeterminado es **adPersistADTG**.

## <a name="remarks"></a>Comentarios

El método **Save** se puede invocar únicamente en un objeto **Recordset** abierto. Utilice el método [Open](open-method-ado-recordset.md) para restaurar posteriormente el objeto **Recordset** desde *Destination*.

Si se estableció la propiedad [Filter](filter-property-ado.md) para el objeto **Recordset**, se guardan únicamente las filas accesibles con el filtro activado. Si el objeto **Recordset** es jerárquico, se guardan el **Recordset** secundario actual y sus elementos secundarios, incluido el objeto **Recordset** primario. Si se invoca el método **Save** de un objeto **Recordset** secundario, se guardan el objeto secundario y todos sus elementos secundarios, pero no se guarda el objeto primario.

La primera vez que se guarda el **conjunto de registros**, la especificación de *Destination* es opcional. Si se omite *Destination*, se creará un nuevo archivo con un nombre establecido en el valor de la propiedad [Origen](source-property-ado-recordset.md) del **conjunto de registros**.

Se omite *Destination* cuando se vuelve a llamar a **Guardar** después de la primera o se producirá un error en tiempo de ejecución. Si se llama posteriormente **Guardar** con un nuevo *destino*, se guarda el **objeto Recordset** en el nuevo destino. Sin embargo, tanto el nuevo destino como el original estarán abiertos.

El método **Save** no cierra el objeto **Recordset** ni el valor especificado por *Destination*, por lo que se puede seguir trabajando con el objeto **Recordset** y se pueden guardar los cambios más recientes. *Destination* permanecerá abierto hasta que se cierre el objeto **Recordset**.

Por motivos de seguridad, el método **Save** sólo permite el uso de configuraciones de seguridad baja y personalizada desde un script ejecutado por Microsoft Internet Explorer. Para obtener una explicación más detallada de los problemas de seguridad, vea el tema sobre los problemas de seguridad de ADO y RDS en Microsoft Internet Explorer, que se encuentra en los artículos técnicos de ActiveX Data Objects (ADO), en la sección de artículos técnicos de Microsoft Data Access.

Si se llama al método **Save** mientras hay en curso una operación asincrónica de recuperación, ejecución o actualización de un objeto **Recordset**, **Save** esperará hasta que finalice la operación asincrónica.

Los registros se guardan comenzando por la primera fila del objeto **Recordset**. Cuando finalice el método **Save**, la posición de fila actual se moverá hasta la primera fila del objeto **Recordset**.

Para obtener los mejores resultados, establezca el valor de la propiedad [CursorLocation](cursorlocation-property-ado.md) en **adUseClient** con el método **Save**. Si el proveedor no admite todas las funciones necesarias para guardar los objetos **Recordset**, el Servicio de cursores las proporcionará.

Cuando se almacena un objeto **Recordset** con el valor de la propiedad **CursorLocation** establecido en **adUseServer**, la función de actualización del objeto **Recordset** es limitada. Normalmente, solo se permiten eliminaciones, inserciones y actualizaciones de una sola tabla (según la funcionalidad del proveedor). El método [Resync](resync-method-ado.md) tampoco está disponible en esta configuración.


> [!NOTE]
> <P>[!NOTA] El almacenamiento de un objeto <STRONG>Recordset</STRONG> con <STRONG>campos</STRONG> de tipo <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> o <STRONG>adIUnknown</STRONG> no lo admite ADO y puede generar resultados impredecibles.</P>



Sólo los **filtros** con el formato de las cadenas de criterios (por ejemplo, FechaPedido \> ' 12/31/1999 ') afectan al contenido de un **objeto Recordset**de persistentes. Los filtros creados con una matriz de **marcadores** o mediante un valor de **FilterGroupEnum** no afectan al contenido del objeto **Recordset** almacenado. Estas reglas se aplican a los objetos **Recordset** creados con cursores de cliente o de servidor.

Debido a que el parámetro *Destination* puede aceptar cualquier objeto que admita la interfaz IStream de OLE DB, puede guardar un **objeto Recordset** directamente en el objeto Response de ASP. Para obtener más información, vea [Escenario de almacenamiento de un objeto Recordset en formato XML](xml-recordset-persistence-scenario.md).

También se puede guardar un objeto **Recordset** con formato XML en una instancia de un objeto DOM MSXML, tal y como se muestra en el código siguiente de Visual Basic:


> [!NOTE]
> <P>[!NOTA] Existen dos limitaciones cuando se guardan objetos <STRONG>Recordset</STRONG> jerárquicos (formas de datos) en formato XML: no se puede guardar en XML si el objeto <STRONG>Recordset</STRONG> jerárquico contiene actualizaciones pendientes y no se puede guardar un objeto <STRONG>Recordset</STRONG> jerárquico parametrizado.</P>



Un objeto Recordset guardado en formato XML se guarda mediante el formato UTF-8. Cuando ese archivo se carga en un objeto Stream de ADO, este objeto no intentará abrir un objeto Recordset de la secuencia, a menos que la propiedad Charset de la secuencia tenga el valor apropiado para el formato UTF-8.

