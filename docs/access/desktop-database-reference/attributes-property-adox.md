---
title: Propiedad Attributes (ADOX)
TOCTitle: Attributes property (ADOX)
ms:assetid: d5227b10-4a9b-5a57-d5ab-bbdd3e89aa95
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250072(v=office.15)
ms:contentKeyID: 48547959
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14a4c719723767be8cb8e7e2f8ed02b5d2d4a143
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296951"
---
# <a name="attributes-property-adox"></a>Propiedad Attributes (ADOX)


**Se aplica a:** Access 2013, Office 2013

Describe características de columna.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Long**. El valor especifica características de la tabla representada por el objeto [Column](column-object-adox.md) y puede ser una combinación de constantes [ColumnAttributesEnum](columnattributesenum.md). El valor predeterminado es cero (0), que no es **adColFixed** ni **adColNullable**.

