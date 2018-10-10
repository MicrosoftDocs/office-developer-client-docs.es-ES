---
title: Utilizar ADO para publicaciones en Internet
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e2d939f8583fdfd98ed1ae8e51a5bbfe792e486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486307"
---
# <a name="using-ado-for-internet-publishing"></a>Utilizar ADO para publicaciones en Internet


**Se aplica a**: Access 2013 | Office 2013



[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) muestra un ejemplo específico de cómo obtener acceso a datos heterogéneos con ADO. Si bien los ejemplos de esta sección son específicos del proveedor de publicaciones en Internet, los principios descritos deben ser similares en el caso de utilizar ADO con otros proveedores para obtener acceso a datos heterogéneos, como un proveedor para obtener acceso a un almacén de correo electrónico.

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

