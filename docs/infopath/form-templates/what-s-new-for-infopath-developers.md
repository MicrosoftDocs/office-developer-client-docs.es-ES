---
title: Novedades para programadores de InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- what's new [infopath 2007],developer features [InfoPath 2007],InfoPath 2007, what's new,new features [InfoPath 2007]
localization_priority: Normal
ms.assetid: d0ad3111-bd41-4f35-8a34-62c17f20fc19
description: InfoPath está diseñado para facilitar la creación de aplicaciones enriquecidas basadas en formularios en la plataforma Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 y InfoPath Forms Services disponen de numerosas funciones para desarrolladores. InfoPath Forms Services, que está disponible en SharePoint Server 2013, le permite implementar una plantilla de formulario de InfoPath en un SharePoint Server, de tal modo que aquellos usuarios que no tengan el cliente enriquecido de InfoPath puedan abrir y rellenar formularios de InfoPath en un explorador web.
ms.openlocfilehash: 5d469dfb99290054008271867f24d947a42efeee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303195"
---
# <a name="whats-new-for-infopath-developers"></a><span data-ttu-id="bb463-106">Novedades para programadores de InfoPath</span><span class="sxs-lookup"><span data-stu-id="bb463-106">What's New for InfoPath Developers</span></span>

<span data-ttu-id="bb463-p102">InfoPath está diseñado para facilitar la creación de aplicaciones enriquecidas basadas en formularios en la plataforma Microsoft SharePoint Server. Microsoft InfoPath 2013, Microsoft SharePoint Server 2013 y InfoPath Forms Services disponen de numerosas funciones para desarrolladores. InfoPath Forms Services, que está disponible en SharePoint Server 2013, le permite implementar una plantilla de formulario de InfoPath en un SharePoint Server, de tal modo que aquellos usuarios que no tengan el cliente enriquecido de InfoPath puedan abrir y rellenar formularios de InfoPath en un explorador web.</span><span class="sxs-lookup"><span data-stu-id="bb463-p102">InfoPath is designed to make it easy to build rich forms-based applications on the Microsoft SharePoint Server platform. Microsoft InfoPath 2013 in conjunction with Microsoft SharePoint Server 2013 and InfoPath Forms Services have many features for developers. InfoPath Forms Services, which is available in SharePoint Server 2013, enables you to deploy an InfoPath form template to a SharePoint Server so that users without the InfoPath rich client can open and fill out InfoPath forms in a Web browser.</span></span>
  
<span data-ttu-id="bb463-p103">Las plantillas de formulario creadas con InfoPath 2013 siguen admitiendo lógica empresarial escrita con relación a las clases y los miembros del espacio de nombres **Microsoft.Office.InfoPath**, que funciona de la misma forma con un formulario abierto en InfoPath Filler que con un formulario abierto en un explorador web. Usando la lógica empresarial escrita en este modelo de objetos administrados y trabajando con las funciones de comprobación de diseño de InfoPath Designer, puede crear una plantilla de formulario sencilla e implementarla en una biblioteca de documentos configurada correctamente en SharePoint Server 2013, que se iniciará en InfoPath Filler y en un explorador web.</span><span class="sxs-lookup"><span data-stu-id="bb463-p103">Form templates created using InfoPath 2013 continue to support business logic written against the classes and members of the **Microsoft.Office.InfoPath** namespace, which works the same way for a form opened in the InfoPath filler and in a form opened in a Web browser. By using business logic written to this managed object model, and by working with design checking features in InfoPath Designer, you can create a single form template that you can deploy to an appropriately configured document library on SharePoint Server 2013, which will run in both the InfoPath filler and in a Web browser.</span></span> 
  
## <a name="new-features-and-improvements"></a><span data-ttu-id="bb463-112">Características y mejoras</span><span class="sxs-lookup"><span data-stu-id="bb463-112">New Features and Improvements</span></span>

<span data-ttu-id="bb463-113">En las secciones siguientes se describen brevemente las funciones y mejoras de interés para desarrolladores de InfoPath:</span><span class="sxs-lookup"><span data-stu-id="bb463-113">The following sections briefly describe these features and improvements that are interesting to InfoPath developers:</span></span>
  
- <span data-ttu-id="bb463-114">Nueva forma de escribir y modificar código</span><span class="sxs-lookup"><span data-stu-id="bb463-114">New Way to Write and Edit Code</span></span>
    
- <span data-ttu-id="bb463-115">Soluciones de espacio aislado de SharePoint</span><span class="sxs-lookup"><span data-stu-id="bb463-115">SharePoint Sandboxed Solutions</span></span>
    
- <span data-ttu-id="bb463-116">Publicar formularios con un solo clic</span><span class="sxs-lookup"><span data-stu-id="bb463-116">Publish Forms with One Click</span></span>
    
- <span data-ttu-id="bb463-117">Mejorar los formularios de lista de SharePoint</span><span class="sxs-lookup"><span data-stu-id="bb463-117">Enhance SharePoint List Forms</span></span>
    
- <span data-ttu-id="bb463-118">Hospedar formularios en portales mediante el elemento web Formulario de InfoPath</span><span class="sxs-lookup"><span data-stu-id="bb463-118">Host Forms on Portal Pages using the InfoPath Form web part</span></span>
    
- <span data-ttu-id="bb463-119">Formularios web más complejos</span><span class="sxs-lookup"><span data-stu-id="bb463-119">Richer Web Forms</span></span>
    
- <span data-ttu-id="bb463-120">Formularios de explorador compatibles con los estándares</span><span class="sxs-lookup"><span data-stu-id="bb463-120">Standards Compliant Browser Forms</span></span>
    
- <span data-ttu-id="bb463-121">Proporcionar seguridad e integridad de la información mejoradas con firmas digitales</span><span class="sxs-lookup"><span data-stu-id="bb463-121">Provide Enhanced Information Security and Integrity with Digital Signatures</span></span>
    
- <span data-ttu-id="bb463-122">Controles</span><span class="sxs-lookup"><span data-stu-id="bb463-122">New Controls</span></span>
    
## <a name="new-way-to-write-and-edit-code"></a><span data-ttu-id="bb463-123">Nueva forma de escribir y modificar código</span><span class="sxs-lookup"><span data-stu-id="bb463-123">New Way to Write and Edit Code</span></span>

<span data-ttu-id="bb463-p104">El IDE de Microsoft Visual Studio Tools for Applications integrado en InfoPath 2010 se ha eliminado en InfoPath 2013. Para escribir o modificar código en InfoPath 2013, ahora debe disponer de Visual Studio 2012 con el complemento [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) instalado. Aunque la experiencia de programación no ha cambiado en lo esencial, ahora puede aprovechar toda la experiencia de desarrollo de Visual Studio al escribir código administrado para sus formularios de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="bb463-p104">The Microsoft Visual Studio Tools for Applications IDE that was integrated with InfoPath 2010 has been removed in InfoPath 2013. To write or edit form code in InfoPath 2013 now requires Visual Studio 2012 with the [Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) add-on installed. The programming experience itself has not fundamentally changed, but you can now use the full Visual Studio development experience when writing managed code for your InfoPath forms.</span></span> 
  
<span data-ttu-id="bb463-127">En las siguientes secciones se describen las funciones integradas originalmente en InfoPath 2010 y SharePoint Server 2010 y que continúan aportando valor a los desarrolladores que usan InfoPath 2013 y SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bb463-127">The following sections describe features that were first added in InfoPath 2010 and SharePoint Server 2010 and continue to add value for developers using InfoPath 2013 and SharePoint Server 2013.</span></span>
  
## <a name="sharepoint-server-sandboxed-solutions"></a><span data-ttu-id="bb463-128">Soluciones de espacio aislado de SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="bb463-128">SharePoint Server Sandboxed Solutions</span></span>

<span data-ttu-id="bb463-p105">Con InfoPath, implementar formularios con código en SharePoint Server 2013 es más fácil que nunca. En Office InfoPath 2007, era necesario que un administrador de granja de servidores de SharePoint aprobara y cargara todos los formularios con código. La compatibilidad con soluciones de espacio aislado en SharePoint Server 2013 permite ahora a los diseñadores de formularios con permisos de administración de colecciones de sitios publicar la mayoría de los formularios con código, directamente en sus sitios de SharePoint. Un parámetro de cuota de recursos permite limitar el uso excesivo de recursos en el servidor. El administrador de la colección de sitios mantiene el control de la solución y puede tomar decisiones de confianza relacionadas con ella. El administrador de la granja de servidores puede no intervenir. Para más información sobre cómo publicar plantillas de formulario de InfoPath como soluciones de espacio aislado, vea [Publicar formularios con código](publishing-forms-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="bb463-p105">With InfoPath, it is easier than ever to deploy forms with code to SharePoint Server 2013. In Office InfoPath 2007, all forms with code had to be approved and uploaded by a SharePoint farm administrator. With support for sandboxed solutions in SharePoint Server 2013, form designers that have site collection administration permissions can now publish most forms with code, directly to their SharePoint sites. A resource quota setting on the server limits excessive resource usage. The site collection administrator remains in control and makes trust decisions about the solution. The farm administrator can be hands-off. For more information about publishing InfoPath form templates as sandboxed solutions, see [Publishing Forms with Code](publishing-forms-with-code.md).</span></span>
  
## <a name="publish-forms-with-one-click"></a><span data-ttu-id="bb463-136">Publicar formularios con un solo clic</span><span class="sxs-lookup"><span data-stu-id="bb463-136">Publish Forms with One Click</span></span>

<span data-ttu-id="bb463-p106">InfoPath está diseñado para que le resulte más sencillo que nunca publicar actualizaciones en sus formularios. Después de publicar una plantilla de formulario por primera vez, en lugar de tener que pasar por varios cuadros de diálogo, puede llevar a cabo esta tarea con un solo clic en el nuevo botón **Publicación rápida**, que está disponible en la **Barra de herramientas de acceso rápido**, y en la nueva Microsoft Office Backstage, disponible al hacer clic en la pestaña **Archivo**.</span><span class="sxs-lookup"><span data-stu-id="bb463-p106">InfoPath is designed to make it easier than ever to publish updates to your forms.. After the first time that you publish a form template, instead of clicking through several dialog boxes, you can complete this task with one click of the new **Quick Publish** button, which is available on the **Quick Access Toolbar**, and in the new Microsoft Office Backstage, which is available by clicking the **File** tab.</span></span> 
  
## <a name="enhance-sharepoint-list-forms"></a><span data-ttu-id="bb463-139">Mejorar formularios de lista de SharePoint</span><span class="sxs-lookup"><span data-stu-id="bb463-139">Enhance SharePoint List Forms</span></span>

<span data-ttu-id="bb463-p107">Con InfoPath, ahora puede ampliar y mejorar los formularios usados para crear, modificar y ver elementos en una lista de SharePoint. Al abrir una lista y hacer clic en la pestaña **Lista** de **Herramientas de listas** y, después, en **Personalizar formulario**, puede generar automáticamente un formulario de InfoPath similar al formulario de lista de SharePoint predeterminado que viene incluido. Después, puede personalizar y mejorar este formulario modificando el diseño, creando vistas adicionales y agregando reglas y validación de datos en InfoPath. Cuando termine de modificar el formulario de lista mejorado, puede publicarlo en SharePoint con la nueva función de publicación con un solo clic de InfoPath.</span><span class="sxs-lookup"><span data-stu-id="bb463-p107">Using InfoPath, you can now extend and enhance the forms used for creating, editing and viewing items in a SharePoint list. By opening a list, clicking the **List** tab under **List Tools**, and then clicking **Customize Form**, you can auto generate an InfoPath form which resembles the default, out-of-the-box SharePoint list form. You can then customize and enhance this form by modifying the layout, creating additional views, and adding rules and data validation in InfoPath. When you are finished modifying your improved list form, you can publish it to SharePoint using the new one-click publish feature in InfoPath.</span></span>
  
## <a name="host-forms-on-portal-pages-using-the-infopath-form-web-part"></a><span data-ttu-id="bb463-144">Hospedar formularios en portales mediante el elemento web Formulario de InfoPath</span><span class="sxs-lookup"><span data-stu-id="bb463-144">Host Forms on Portal Pages using the InfoPath Form web part</span></span>

<span data-ttu-id="bb463-145">En SharePoint Server 2013, resulta más fácil que nunca hospedar los formularios en páginas web con el nuevo **Elemento web Formulario de Infopath**.</span><span class="sxs-lookup"><span data-stu-id="bb463-145">In SharePoint Server 2013, it is easier than ever to host your forms on Web pages using the new **InfoPath Form web part**.</span></span> <span data-ttu-id="bb463-146">En Microsoft Office SharePoint Server 2007, los usuarios que deseen hospedar los formularios de InfoPath en páginas web deben escribir el código de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bb463-146">In Microsoft Office SharePoint Server 2007, users who want host their InfoPath forms on Web pages have to write code in Visual Studio.</span></span> <span data-ttu-id="bb463-147">Ahora, sin tener que escribir una sola línea de código, puede agregar el **elemento web Formulario de InfoPath** a una página de elementos web y apuntarla al formulario publicado. Puede usar el **elemento web Formulario de InfoPath** para hospedar cualquier formulario explorador de InfoPath que se publique en una biblioteca de formularios o lista de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bb463-147">Now, without writing a single line of code, you can add the **InfoPath Form web part** to a Web Parts page and point it to your published form.You can use the **InfoPath Form web part** to host any InfoPath browser form that is published to a SharePoint list or form library.</span></span> <span data-ttu-id="bb463-148">También puede conectarse a otros elementos web en la página para enviar o recibir datos.</span><span class="sxs-lookup"><span data-stu-id="bb463-148">You can also connect it to other Web Parts on the page to send or receive data.</span></span> <span data-ttu-id="bb463-149">Para obtener más información sobre cómo usar el **elemento web Formulario de InfoPath**, vea [Trabajar con el elemento web Formulario de InfoPath](https://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) en el SDK de SharePoint 2010.</span><span class="sxs-lookup"><span data-stu-id="bb463-149">For more information about how to use the **InfoPath Form web part**, see [Working with the InfoPath Form web part](https://msdn.microsoft.com/library/bb87e126-1a07-45aa-af36-b294df3a2576%28Office.15%29.aspx) in the SharePoint 2010 SDK.</span></span> 
  
## <a name="richer-web-forms"></a><span data-ttu-id="bb463-150">Formularios web más complejos</span><span class="sxs-lookup"><span data-stu-id="bb463-150">Richer Web Forms</span></span>

<span data-ttu-id="bb463-p109">La diferencia en las características entre formularios de cliente y explorador se ha reducido, generando una experiencia de rellenado de formularios más uniforme para todos los usuarios. Los controles y funcionalidades que se admiten actualmente en los formularios de explorador incluyen:</span><span class="sxs-lookup"><span data-stu-id="bb463-p109">The feature gap between client and browser forms has been narrowed, creating a more consistent form filling experience for all users. Controls and functionality that are now supported in browser forms include the following:</span></span>
  
- <span data-ttu-id="bb463-153">Listas con viñetas, numeradas y simples</span><span class="sxs-lookup"><span data-stu-id="bb463-153">Bulleted, numbered, and plain lists</span></span>
    
- <span data-ttu-id="bb463-154">Cuadros de lista de selección múltiple</span><span class="sxs-lookup"><span data-stu-id="bb463-154">Multiple selection list boxes</span></span>
    
- <span data-ttu-id="bb463-155">Cuadros combinados</span><span class="sxs-lookup"><span data-stu-id="bb463-155">Combo boxes</span></span>
    
- <span data-ttu-id="bb463-156">Botones de imagen</span><span class="sxs-lookup"><span data-stu-id="bb463-156">Picture buttons</span></span>
    
- <span data-ttu-id="bb463-157">Capacidades de hipervínculo</span><span class="sxs-lookup"><span data-stu-id="bb463-157">Hyperlink capabilities</span></span>
    
- <span data-ttu-id="bb463-158">Sección y grupo de opciones</span><span class="sxs-lookup"><span data-stu-id="bb463-158">Choice group and section</span></span> 
    
- <span data-ttu-id="bb463-159">Controles de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="bb463-159">Date and time controls</span></span>
    
- <span data-ttu-id="bb463-160">Selector de personas o grupos</span><span class="sxs-lookup"><span data-stu-id="bb463-160">Person/group pickers</span></span>
    
- <span data-ttu-id="bb463-161">Funcionalidad de filtrado</span><span class="sxs-lookup"><span data-stu-id="bb463-161">Filtering functionality</span></span>
    
## <a name="standards-compliant-browser-forms"></a><span data-ttu-id="bb463-162">Formularios de explorador compatibles con los estándares</span><span class="sxs-lookup"><span data-stu-id="bb463-162">Standards Compliant Browser Forms</span></span>

<span data-ttu-id="bb463-163">Ahora los formularios de explorador de InfoPath cumplen las Instrucciones de accesibilidad a contenido web 2.0 (WCAG 2.0) AA, lo que permite a los diseñadores crear formularios que puedan estar disponibles para usuarios con discapacidades.</span><span class="sxs-lookup"><span data-stu-id="bb463-163">InfoPath browser forms are now compliant with Web Content Accessibility Guidelines 2.0 (WCAG 2.0) AA, which enables form designers to create forms that are available for users with disabilities.</span></span>
  
## <a name="provide-enhanced-information-security-and-integrity-with-digital-signatures"></a><span data-ttu-id="bb463-164">Proporcionar seguridad e integridad de la información mejoradas con firmas digitales</span><span class="sxs-lookup"><span data-stu-id="bb463-164">Provide Enhanced Information Security and Integrity with Digital Signatures</span></span>

<span data-ttu-id="bb463-p110">InfoPath admite contenido firmado digitalmente de Cryptography Next Generation (CNG). Para asegurar la integridad de la información que contienen los formularios, el cliente de InfoPath y SharePoint Server 2013 proporcionan los controles necesarios para habilitar escenarios de firma única, cofirma y contrafirma de todo el formulario o secciones del mismo. Los formularios se pueden firmar en Internet Explorer con el control ActiveX de línea de firma. Los formularios firmados se pueden ver en cualquier explorador compatible con SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bb463-p110">InfoPath supports Cryptography Next Generation (CNG) digitally signed content. To help you ensure the integrity of the information that is contained in your forms, the InfoPath client and SharePoint Server 2013 provide the controls necessary to enable single, co-sign, and counter-sign scenarios for the full form or sections of the form. Forms can be signed in Internet Explorer using the ActiveX signature line control. Signed forms can be viewed in any browser supported by SharePoint Server 2013.</span></span>
  
## <a name="new-controls"></a><span data-ttu-id="bb463-169">Controles</span><span class="sxs-lookup"><span data-stu-id="bb463-169">New Controls</span></span>

<span data-ttu-id="bb463-p111">InfoPath proporciona un conjunto de controles más completo que se puede agregar a sus formularios. En la lista siguiente se describen de manera breve algunos de los nuevos controles disponibles:</span><span class="sxs-lookup"><span data-stu-id="bb463-p111">InfoPath provides a richer set of controls that can be added to your forms. The following list briefly describes some of the new controls:</span></span>
  
- <span data-ttu-id="bb463-172">**Botón de imagen**: en lugar de un rectángulo gris, use cualquier imagen como botón en el formulario.</span><span class="sxs-lookup"><span data-stu-id="bb463-172">**Picture Button** — Instead of a gray rectangle; use any image as a button in your form.</span></span> 
    
- <span data-ttu-id="bb463-173">**Hipervínculo**: permita que los usuarios escriban sus propios hipervínculos cuando rellenan formularios.</span><span class="sxs-lookup"><span data-stu-id="bb463-173">**Hyperlink** — Enable users to enter their own hyperlinks when filling out forms.</span></span> 
    
- <span data-ttu-id="bb463-174">**Selector de personas o grupos**: permita que los usuarios comprueben y consulten nombres de cuenta y grupos cuando rellenan formularios.</span><span class="sxs-lookup"><span data-stu-id="bb463-174">**Person/Group Picker** — Enable users to check and query account names and groups when filling out forms.</span></span> 
    
- <span data-ttu-id="bb463-175">**Selector de entidad**: permita que los usuarios seleccionen valores desde listas externas en un servidor que inicia SharePoint Server 2013.</span><span class="sxs-lookup"><span data-stu-id="bb463-175">**Entity Picker** — Enable users to select values from external lists on a server that is running SharePoint Server 2013 when forms.</span></span> 
    
- <span data-ttu-id="bb463-176">**Línea de firma**: proporcione a los usuarios una línea de firma o imagen de sello, por ejemplo, un sello inkan o hanko, cuando firmen digitalmente formularios.</span><span class="sxs-lookup"><span data-stu-id="bb463-176">**Signature Line** — Provide users with a signature line or stamp image, such as an inkan or hanko seal, when digitally signing forms.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bb463-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb463-177">See also</span></span>



[<span data-ttu-id="bb463-178">Desarrollo de plantillas de formulario de InfoPath con código</span><span class="sxs-lookup"><span data-stu-id="bb463-178">Developing InfoPath Form Templates with Code</span></span>](developing-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="bb463-179">Programar plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="bb463-179">Developing Form Templates Using the InfoPath 2003 Object Model</span></span>](developing-form-templates-using-the-infopath-2003-object-model.md)

