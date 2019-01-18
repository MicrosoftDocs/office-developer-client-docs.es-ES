---
title: Procedimientos recomendados para desarrollar complementos de Outlook administrados
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 474a43c17360979b4b25ccb55c0ed48b2c9d2ef7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28723099"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="b1a09-102">Procedimientos recomendados para desarrollar complementos de Outlook administrados</span><span class="sxs-lookup"><span data-stu-id="b1a09-102">Best practices in developing managed Outlook add-ins</span></span>

<span data-ttu-id="b1a09-p101">Incluso cuando los ensamblados de interoperabilidad de Outlook le permiten escribir soluciones administradas que interoperan con Outlook, Outlook es anterior a .NET Framework y está diseñado para proporcionar compatibilidad de programación a través de lenguajes no administrados como Visual Basic para Aplicaciones (VBA) y Visual Basic. En este tema se muestran las áreas principales que debe conocer al desarrollar un complemento administrado para Outlook.</span><span class="sxs-lookup"><span data-stu-id="b1a09-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- <span data-ttu-id="b1a09-105">[Systematically releasing objects](systematically-releasing-objects.md) (Lanzar objetos sistemáticamente)</span><span class="sxs-lookup"><span data-stu-id="b1a09-105">[Systematically releasing objects](systematically-releasing-objects.md)</span></span>
- <span data-ttu-id="b1a09-106">[Using a separate application domain to avoid crashing](using-a-separate-application-domain-to-avoid-crashing.md) (Uso de un dominio de aplicación independiente para evitar el bloqueo)</span><span class="sxs-lookup"><span data-stu-id="b1a09-106">[Using a separate application domain to avoid crashing](using-a-separate-application-domain-to-avoid-crashing.md)</span></span>
- <span data-ttu-id="b1a09-107">[Using a trusted application object provided by Office Developer Tools for Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md) (Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="b1a09-107">[Using a trusted application object provided by Office Developer Tools for Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)</span></span>
- <span data-ttu-id="b1a09-108">[Scoping variables appropriately in event handlers](scoping-variables-appropriately-in-event-handlers.md) (Configuración del ámbito de variables correctamente en controladores de eventos)</span><span class="sxs-lookup"><span data-stu-id="b1a09-108">[Scoping variables appropriately in event handlers](scoping-variables-appropriately-in-event-handlers.md)</span></span>
- <span data-ttu-id="b1a09-109">[Avoiding unsupported technologies in managed Outlook add-ins](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md) (Evitar tecnologías no admitidas en los complementos administrados de Outlook)</span><span class="sxs-lookup"><span data-stu-id="b1a09-109">[Avoiding unsupported technologies in managed Outlook add-ins](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)</span></span>
- <span data-ttu-id="b1a09-110">[Using late binding if depending on multiple versions of Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md) (Uso del enlace en tiempo de ejecución cuando se depende de varias versiones de Outlook)</span><span class="sxs-lookup"><span data-stu-id="b1a09-110">[Using late binding if depending on multiple versions of Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)</span></span>

