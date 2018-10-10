---
title: Consideraciones de seguridad XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3120db77ba89aee1036de4d6fa85df73c21d26d9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485990"
---
# <a name="xml-security-considerations"></a>Consideraciones de seguridad XML


**Se aplica a**: Access 2013 | Office 2013

## <a name="xml-security-considerations"></a>Consideraciones de seguridad XML

Los métodos **Save** y **Open** de ADO del objeto **Recordset** no se consideran operaciones seguras para ejecutarse en Internet Explorer. Por ello, si estos métodos se usan en código de script que se ejecuta en una aplicación o en un control hospedado en un explorador, la configuración de seguridad del explorador influirá en su comportamiento.

Internet Explorer 5 proporciona restricciones de seguridad para dichas operaciones de forma predeterminada en las zonas de Internet. En esa configuración, el objeto **Recordset** no puede obtener acceso al sistema de archivos local en el cliente ni tener acceso a ningún origen de datos fuera del dominio del servidor desde el que se ha descargado la página. Específicamente, cuando se ejecuta en el equipo que hospeda el explorador, un objeto **Recordset** sólo se puede guardar en un archivo si se encuentra en el mismo servidor desde el que se descargó la página. Del mismo modo, se puede abrir un objeto **Recordset** cargándolo desde un archivo únicamente si ese archivo está en el mismo servidor desde el que se descargó la página.

Para obtener más información sobre la seguridad en Internet Explorer, vea el artículo técnico "ADO and RDS Security Issues in Microsoft Internet Explorer" (en inglés).

