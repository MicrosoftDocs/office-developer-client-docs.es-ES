---
title: Utilizar ADO para publicaciones en Internet
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e63e765461eec1c89f3e3dc04d35f1bf88a3c578
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997626"
---
# <a name="using-ado-for-internet-publishing"></a>Utilizar ADO para publicación en Internet


**Se aplica a**: Access 2013, Office 2013



[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) muestra un ejemplo específico de cómo obtener acceso a datos heterogéneos con ADO. Mientras que los ejemplos de esta sección será específicos para usar el proveedor de publicación en Internet, los principios mostrados deberían ser similares al uso de ADO con otros proveedores de datos heterogéneos, como un proveedor a un almacén de correo electrónico.

## <a name="urls"></a>Localizadores URL

Se pueden usar Localizadores uniformes de recursos (URL) como alternativa a las cadenas de conexión y al texto de comando para especificar los orígenes de datos y la ubicación de los archivos y directorios. Se pueden utilizar localizadores URL con los objetos [Connection](connection-object-ado.md) y **Recordset** existentes así como con los objetos **Record** y **Stream**.

Para obtener más información sobre el uso de los localizadores URL, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).

## <a name="record-fields"></a>Campos de registro

La diferencia distintiva entre los datos heterogéneos y los datos homogéneos reside en que, en el primer caso, cada fila de datos o **registro** puede tener un conjunto diferente de columnas o **campos**. En el caso de los datos homogéneos, cada fila tiene el mismo conjunto de columnas. Para obtener más información sobre los campos específicos del proveedor de publicaciones en Internet, vea [Registros y campos proporcionados por el proveedor](records-and-provider-supplied-fields.md).

## <a name="appending-new-fields"></a>Anexar campos nuevos

Se han mejorado varios objetos de ADO para que funcionen conjuntamente con los objetos **Record** y **Stream**.

  - El método [Append](fields-collection-ado.md) de la colección [Fields](append-method-ado.md), que crea y agrega un objeto [Field](field-object-ado.md) a la colección, también puede especificar el valor de **Field**.

  - El método [Update](update-method-ado.md) finaliza la adición o la eliminación de campos de la colección.

  - Como método abreviado y una alternativa al método **Append**, se pueden crear campos asignando simplemente un valor a un campo sin definir o un campo anteriormente eliminado.

## <a name="see-also"></a>Vea también

- [Temas de escenario de Internet Publishing](internet-publishing-scenario.md)