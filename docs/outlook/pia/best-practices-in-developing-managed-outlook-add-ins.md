---
title: Procedimientos recomendados para desarrollar complementos de Outlook administrados
TOCTitle: Best practices in developing managed Outlook add-ins
ms:assetid: a03246f6-2ca5-4fcb-8e63-a11cfbc8d9a0
ms:mtpsurl: https://msdn.microsoft.com/library/Bb611563(v=office.15)
ms:contentKeyID: 55119784
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 87573980836d63d751302b0efcec0952331b7fc4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406865"
---
# <a name="best-practices-in-developing-managed-outlook-add-ins"></a><span data-ttu-id="fb8a6-102">Procedimientos recomendados para desarrollar complementos de Outlook administrados</span><span class="sxs-lookup"><span data-stu-id="fb8a6-102">Best Practices in Developing Managed Outlook Add-Ins</span></span>

<span data-ttu-id="fb8a6-p101">Incluso cuando los ensamblados de interoperabilidad de Outlook le permiten escribir soluciones administradas que interoperan con Outlook, Outlook es anterior a .NET Framework y está diseñado para proporcionar compatibilidad de programación a través de lenguajes no administrados como Visual Basic para Aplicaciones (VBA) y Visual Basic. En este tema se muestran las áreas principales que debe conocer al desarrollar un complemento administrado para Outlook.</span><span class="sxs-lookup"><span data-stu-id="fb8a6-p101">Even though the Outlook interop assemblies allow you to write managed solutions that interoperate with Outlook, Outlook predates the .NET Framework and is designed to support programmability through unmanaged languages such as Visual Basic for Applications (VBA) and Visual Basic. This topic lists the top areas that you should be aware of when you develop a managed add-in for Outlook.</span></span>

- <span data-ttu-id="fb8a6-105">[Systematically releasing objects](systematically-releasing-objects.md) (Lanzar objetos sistemáticamente)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-105">[Systematically Releasing Objects](systematically-releasing-objects.md)</span></span>
- <span data-ttu-id="fb8a6-106">[Using a separate application domain to avoid crashing](using-a-separate-application-domain-to-avoid-crashing.md) (Uso de un dominio de aplicación independiente para evitar el bloqueo)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-106">[Using a Separate Application Domain to Avoid Crashing](using-a-separate-application-domain-to-avoid-crashing.md)</span></span>
- <span data-ttu-id="fb8a6-107">[Using a trusted application object provided by Office Developer Tools for Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md) (Usar un objeto de la aplicación de confianza proporcionado por Office Developer Tools para Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-107">[Using a trusted application object provided by Office Developer Tools for Visual Studio](using-a-trusted-application-object-provided-by-office-developer-tools-for-visual-studio.md)</span></span>
- <span data-ttu-id="fb8a6-108">[Scoping variables appropriately in event handlers](scoping-variables-appropriately-in-event-handlers.md) (Configuración del ámbito de variables correctamente en controladores de eventos)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-108">[Scoping Variables Appropriately in Event Handlers](scoping-variables-appropriately-in-event-handlers.md)</span></span>
- <span data-ttu-id="fb8a6-109">[Avoiding unsupported technologies in managed Outlook add-ins](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md) (Evitar tecnologías no admitidas en los complementos administrados de Outlook)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-109">[Avoiding Unsupported Technologies in Managed Outlook Add-ins](avoiding-unsupported-technologies-in-managed-outlook-add-ins.md)</span></span>
- <span data-ttu-id="fb8a6-110">[Using late binding if depending on multiple versions of Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md) (Uso del enlace en tiempo de ejecución cuando se depende de varias versiones de Outlook)</span><span class="sxs-lookup"><span data-stu-id="fb8a6-110">[Using Late Binding If Depending on Multiple Versions of Outlook](using-late-binding-if-depending-on-multiple-versions-of-outlook.md)</span></span>

