---
title: Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio
TOCTitle: Using a trusted application object provided by Office Developer Tools for Visual Studio
ms:assetid: 3778122f-f60e-48e7-8e72-f3aef168bae2
ms:mtpsurl: https://msdn.microsoft.com/library/Bb622502(v=office.15)
ms:contentKeyID: 55119787
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7b56e59b19f1c9a0ee4c730f14200c3e501f5290
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406116"
---
# <a name="using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio"></a><span data-ttu-id="b7f2b-102">Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b7f2b-102">Using a trusted Application object provided by Office Developer Tools for Visual Studio</span></span>

<span data-ttu-id="b7f2b-103">Si está desarrollando un complemento administrado mediante Office Developer Tools para Visual Studio, use siempre el objeto [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) que proporciona Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b7f2b-103">If you are developing a managed add-in by using Office Developer Tools for Visual Studio, always use the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object that is provided by Visual Studio.</span></span> 

<span data-ttu-id="b7f2b-104">A menos que desee automatizar una nueva instancia de Outlook, no use la palabra clave New para crear una nueva instancia de Outlook, ya que esta instancia del objeto **Application** no es de confianza desde la perspectiva de la Protección del modelo de objetos de Outlook.</span><span class="sxs-lookup"><span data-stu-id="b7f2b-104">Unless you intend to automate a new instance of Outlook, do not use the New or new keyword to create a new instance of Outlook, as this instance of the **Application** object is not trusted from the perspective of the Outlook Object Model Guard.</span></span> 

<span data-ttu-id="b7f2b-105">Si el complemento usa un instancia del objeto **Application** que no sea de confianza, en función de la versión de Outlook que esté ejecutando el cliente, el complemento invocará de manera predeterminada la Protección del modelo de objetos de Outlook en varios miembros del modelo de objetos.</span><span class="sxs-lookup"><span data-stu-id="b7f2b-105">If your add-in uses an untrusted instance of the **Application** object, depending on the version of Outlook that the client is running, the add-in by default will invoke Outlook's Object Model Guard on a number of members of the object model.</span></span> 

<span data-ttu-id="b7f2b-106">Para obtener más información sobre el comportamiento de la Protección del modelo de objetos, vea [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)) (Cambios en la seguridad de los códigos en Outlook 2007).</span><span class="sxs-lookup"><span data-stu-id="b7f2b-106">For more information about the behavior of the Object Model Guard, see [Code Security Changes in Outlook 2007](https://msdn.microsoft.com/library/bb226709\(v=office.15\)).</span></span> <span data-ttu-id="b7f2b-107">Tenga en cuenta que, aunque el artículo "Code Security Changes in Outlook 2007" hace referencia a los complementos COM que son de confianza de forma predeterminada, este diseño se aplica a las versiones de Outlook a partir de Outlook 2007, y la confianza se aplica de la misma manera a los complementos administrados.</span><span class="sxs-lookup"><span data-stu-id="b7f2b-107">Note that even though the "Code Security Changes in Outlook 2007" article refers to COM add-ins that are trusted by default, this design applies to versions of Outlook since Outlook 2007, and the trust applies to managed add-ins the same way.</span></span> <span data-ttu-id="b7f2b-108">Independiente de que el complemento sea o no administrado, la confianza se basa en el supuesto de que el complemento usa un objeto **Application** de confianza.</span><span class="sxs-lookup"><span data-stu-id="b7f2b-108">Regardless of whether the add-in is managed or not, the trust is based on the assumption that the add-in uses a trusted **Application** object.</span></span>

