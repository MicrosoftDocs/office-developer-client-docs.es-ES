---
title: Source (propiedad, Record ADO)
TOCTitle: Source Property (ADO Record)
ms:assetid: f36f0f5f-4493-d8c5-db4b-c72f5031bcb3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250235(v=office.15)
ms:contentKeyID: 48548670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5e0157bc81e3f7efdb2227b5c5a9e2bc3642a7d2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883956"
---
# <a name="source-property-ado-record"></a>Source (propiedad, Record ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el origen de datos o el objeto representados por el objeto [Record](record-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Variant** que indica la entidad representada por el objeto **Record**.

## <a name="remarks"></a>Comentarios

La propiedad **Source** devuelve el argumento *Source* del método [Open](open-method-ado-record.md) del objeto de **registro** . Puede incluir una cadena de dirección URL absoluta o relativa. Es posible usar una dirección URL absoluta sin establecer la propiedad [ActiveConnection](activeconnection-property-ado.md) para abrir directamente el objeto **Record**. En este caso se crea un objeto **Connection** implícito.

La propiedad **Source** también puede incluir una referencia a un objeto **Recordset** ya abierto, que abre un objeto **Record** que representa a la fila actual del objeto **Recordset**.

La propiedad **Source** también podría incluir una referencia a un objeto [Command](command-object-ado.md) que devuelve una única fila de datos del proveedor.

Si también se establece la propiedad **ActiveConnection**, la propiedad **Source** debe apuntar a algún objeto que exista en el ámbito de esa conexión. Por ejemplo, en los espacios de nombre con estructura de árbol, si la propiedad **Source** incluye una dirección URL absoluta, debe apuntar a un nodo que exista en el ámbito del nodo identificado por la dirección URL en la cadena de conexión. Si la propiedad **Source** incluye una dirección URL relativa, se valida en el contexto establecido por la propiedad **ActiveConnection**.

La propiedad **Source** es de lectura y escritura mientras el objeto **Record** está cerrado y de sólo lectura mientras el objeto **Record** está abierto.

> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente al [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


