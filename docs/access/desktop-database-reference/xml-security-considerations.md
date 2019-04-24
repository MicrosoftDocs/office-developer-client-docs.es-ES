---
title: Consideraciones de seguridad XML
TOCTitle: XML Security Considerations
ms:assetid: ef2c7f59-f5a2-98d1-37c6-42cb35b26a40
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250214(v=office.15)
ms:contentKeyID: 48548575
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 648e7980be19f8af39cdb5e19858ba1ffd16518e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308249"
---
# <a name="xml-security-considerations"></a><span data-ttu-id="89078-102">Consideraciones de seguridad XML</span><span class="sxs-lookup"><span data-stu-id="89078-102">XML security considerations</span></span>


<span data-ttu-id="89078-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89078-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="xml-security-considerations"></a><span data-ttu-id="89078-104">Consideraciones de seguridad XML</span><span class="sxs-lookup"><span data-stu-id="89078-104">XML Security Considerations</span></span>

<span data-ttu-id="89078-p101">Los métodos **Save** y **Open** de ADO del objeto **Recordset** no se consideran operaciones seguras para ejecutarse en Internet Explorer. Por ello, si estos métodos se usan en código de script que se ejecuta en una aplicación o en un control hospedado en un explorador, la configuración de seguridad del explorador influirá en su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="89078-p101">The ADO **Save** and **Open** methods on the **Recordset** object are not considered safe operations to run in Internet Explorer. Thus, if these methods are used in a script code that is running in an application or control that is hosted in a browser, the security configuration of the browser will have an effect on its behavior.</span></span>

<span data-ttu-id="89078-p102">Internet Explorer 5 proporciona restricciones de seguridad para dichas operaciones de forma predeterminada en las zonas de Internet. En esa configuración, el objeto **Recordset** no puede obtener acceso al sistema de archivos local en el cliente ni tener acceso a ningún origen de datos fuera del dominio del servidor desde el que se ha descargado la página. Específicamente, cuando se ejecuta en el equipo que hospeda el explorador, un objeto **Recordset** sólo se puede guardar en un archivo si se encuentra en el mismo servidor desde el que se descargó la página. Del mismo modo, se puede abrir un objeto **Recordset** cargándolo desde un archivo únicamente si ese archivo está en el mismo servidor desde el que se descargó la página.</span><span class="sxs-lookup"><span data-stu-id="89078-p102">Internet Explorer 5 provides security restrictions for such operations by default in the Internet zones. Under that configuration, the **Recordset** cannot make any access to the local file system on the client or access any data sources outside the domain of the server from which the page has been downloaded. Specifically, when running inside the browser host, a **Recordset** can be saved back to a file only if it is on the same server from which the page was downloaded. Similarly, you can open a **Recordset** by loading it from a file only if that file is on the same server from which the page was downloaded.</span></span>

<span data-ttu-id="89078-111">Para obtener más información sobre la seguridad en Internet Explorer, vea el artículo técnico "ADO and RDS Security Issues in Microsoft Internet Explorer" (en inglés).</span><span class="sxs-lookup"><span data-stu-id="89078-111">For more information about security in Internet Explorer, see the technical article "ADO and RDS Security Issues in Microsoft Internet Explorer."</span></span>

