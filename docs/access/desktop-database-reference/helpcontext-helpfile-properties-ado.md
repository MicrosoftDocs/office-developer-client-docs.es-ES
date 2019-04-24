---
title: Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291995"
---
# <a name="helpcontext-helpfile-properties-ado"></a><span data-ttu-id="b0c06-102">Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0c06-102">HelpContext, HelpFile properties (ADO)</span></span>

<span data-ttu-id="b0c06-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0c06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0c06-104">Indican el archivo de Ayuda y el tema asociados a un objeto [Error](error-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b0c06-104">Indicates the help file and topic associated with an [Error](error-object-ado.md) object.</span></span>

## <a name="return-values"></a><span data-ttu-id="b0c06-105">Valores devueltos</span><span class="sxs-lookup"><span data-stu-id="b0c06-105">Return values</span></span>

- <span data-ttu-id="b0c06-106">**HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="b0c06-106">**HelpContextID** — returns a context ID, as a **Long** value, for a topic in a Help file.</span></span>

- <span data-ttu-id="b0c06-107">**HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.</span><span class="sxs-lookup"><span data-stu-id="b0c06-107">**HelpFile** — returns a **String** value that evaluates to a fully resolved path to a Help file.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0c06-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b0c06-108">Remarks</span></span>

<span data-ttu-id="b0c06-p101">Si se especifica un archivo de Ayuda en la propiedad **HelpFile**, la propiedad **ContextoDeAyuda (HelpContext)** se utiliza para mostrar automáticamente el tema de Ayuda que identifica. Si no hay ningún tema de Ayuda pertinente disponible, la propiedad **ContextoDeAyuda (HelpContext)** devuelve cero y la propiedad **HelpFile** devuelve una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="b0c06-p101">If a Help file is specified in the **HelpFile** property, the **HelpContext** property is used to automatically display the Help topic it identifies. If there is no relevant help topic available, the **HelpContext** property returns zero and the **HelpFile** property returns a zero-length string ("").</span></span>

