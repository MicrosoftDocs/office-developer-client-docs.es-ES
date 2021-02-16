---
title: Variables de plantilla
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Las instancias de variables de plantilla (representadas por un elemento templateVariable) especifican los datos de un elemento de fuente de actividades en una plantilla de actividad.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404375"
---
# <a name="template-variables"></a><span data-ttu-id="6bd2b-103">Variables de plantilla</span><span class="sxs-lookup"><span data-stu-id="6bd2b-103">Template variables</span></span>

<span data-ttu-id="6bd2b-104">Las instancias de variables de plantilla (representadas por un **elemento templateVariable)** especifican los datos de un elemento de fuente de actividades en una plantilla de actividad.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-104">Instances of template variables (represented by a **templateVariable** element) specify the data of an activity feed item in an activity template.</span></span> 
  
<span data-ttu-id="6bd2b-105">Para obtener un ejemplo de XML de fuente de actividades, vea [el ejemplo XML de fuente de actividades](activity-feed-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="6bd2b-105">For an example of activity feed XML, see [Activity Feed XML Example](activity-feed-xml-example.md).</span></span>

<span data-ttu-id="6bd2b-106">En la tabla siguiente se muestran los tipos de variables de plantilla admitidas, cada una representada por el valor de enumeración XML correspondiente.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-106">The following table shows the types of supported template variables, each represented by the corresponding XML enumeration value.</span></span>
  
|<span data-ttu-id="6bd2b-107">**Tipo de variable de plantilla**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-107">**Type of template variable**</span></span>|<span data-ttu-id="6bd2b-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-109">**entityVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-109">**entityVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-110">Una persona, grupo o cosa.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-110">A person, group, or thing.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-111">**linkVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-111">**linkVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-112">Un vínculo.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-112">A link.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-113">**listVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-113">**listVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-114">Un grupo de objetos.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-114">A group of objects.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-115">**pictureVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-115">**pictureVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-116">Imagen.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-116">A picture.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-117">**publisherVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-117">**publisherVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-118">El publicador del elemento de fuente de actividades.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-118">The publisher of the activity feed item.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-119">**textVariable**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-119">**textVariable**</span></span> <br/> |<span data-ttu-id="6bd2b-120">Bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-120">A block of text.</span></span>  <br/> |
   
<span data-ttu-id="6bd2b-121">Cada tipo de variable de plantilla tiene elementos necesarios para especificar los datos sobre esa variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-121">Each type of template variable has required elements to specify the data about that variable.</span></span> <span data-ttu-id="6bd2b-122">Las variables de plantilla se especifican de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-122">Template variables are specified as follows:</span></span>
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a><span data-ttu-id="6bd2b-123">Variable de plantilla de lista</span><span class="sxs-lookup"><span data-stu-id="6bd2b-123">List template variable</span></span>

<span data-ttu-id="6bd2b-124">Puede especificar variables de plantilla contenidas en una lista (delimitadas por los elementos **listVariable** y **listItems)** de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6bd2b-124">You can specify template variables that are contained within a list (delimited by the **listVariable** and **listItems** elements) as follows:</span></span> 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
<span data-ttu-id="6bd2b-125">Una variable de plantilla del tipo **listVariable** es un contenedor para objetos.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-125">A template variable of the **listVariable** type is a container for objects.</span></span> <span data-ttu-id="6bd2b-126">Puede contener elementos delimitados por comas (del tipo **linkVariable** o **textVariable)** o imágenes (del tipo **pictureVariable).**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-126">It can contain comma-delimited items (of the **linkVariable** or **textVariable** type) or pictures (of the **pictureVariable** type).</span></span> <span data-ttu-id="6bd2b-127">Las listas pueden contener hasta cinco elementos de vínculo, cinco elementos de texto o cinco imágenes.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-127">Lists can contain up to five link items, five text items, or five pictures.</span></span> 
  
<span data-ttu-id="6bd2b-128">Outlook Social Connector (OSC) localiza los elementos de lista de vínculos o texto de acuerdo con la configuración regional del sistema de Windows.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-128">The Outlook Social Connector (OSC) localizes link or text list items according to the Windows system locale.</span></span>
  
<span data-ttu-id="6bd2b-129">Para analizar y mostrar imágenes correctamente en un elemento de fuente de actividades, debe incluir imágenes en una lista.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-129">To correctly parse and display pictures in an activity feed item, you must include pictures in a list.</span></span> <span data-ttu-id="6bd2b-130">Se cambia el tamaño de todas las imágenes a 52 píxeles de alto.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-130">All pictures are resized to be 52 pixels high.</span></span> <span data-ttu-id="6bd2b-131">No se cambia el tamaño del ancho de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-131">The width of the picture is not resized.</span></span>
  
## <a name="template-variable-elements"></a><span data-ttu-id="6bd2b-132">Elementos de variable de plantilla</span><span class="sxs-lookup"><span data-stu-id="6bd2b-132">Template variable elements</span></span>

<span data-ttu-id="6bd2b-133">En esta sección se tratan los elementos obligatorios y opcionales admitidos para cada tipo de variable de plantilla.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-133">This section covers the required and optional elements supported for each type of template variable.</span></span>
  
### <a name="entityvariable"></a><span data-ttu-id="6bd2b-134">entityVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-134">entityVariable</span></span>

|<span data-ttu-id="6bd2b-135">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-135">**Element**</span></span>|<span data-ttu-id="6bd2b-136">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-136">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-137">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-137">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-138">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-138">The name of the variable.</span></span> <span data-ttu-id="6bd2b-139">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-139">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-140">**id**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-140">**id**</span></span> <br/> |<span data-ttu-id="6bd2b-141">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-141">The unique ID of the user.</span></span> <span data-ttu-id="6bd2b-142">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-142">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-143">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-143">**nameHint**</span></span> <br/> |<span data-ttu-id="6bd2b-144">Nombre que se mostrará en el elemento de fuente.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-144">The name to be displayed in the feed item.</span></span> <span data-ttu-id="6bd2b-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-145">Optional.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-146">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-146">**profileUrl**</span></span> <br/> |<span data-ttu-id="6bd2b-147">Dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de fuente, si el nombre de la persona está presente.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-147">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="6bd2b-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-148">Optional.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-149">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-149">**emailAddress**</span></span> <br/> |<span data-ttu-id="6bd2b-150">La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-150">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="6bd2b-151">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-151">Optional.</span></span>  <br/> |
   
### <a name="linkvariable"></a><span data-ttu-id="6bd2b-152">linkVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-152">linkVariable</span></span>

|<span data-ttu-id="6bd2b-153">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-153">**Element**</span></span>|<span data-ttu-id="6bd2b-154">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-154">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-155">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-155">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-156">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-156">The name of the variable.</span></span> <span data-ttu-id="6bd2b-157">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-157">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-158">**value**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-158">**value**</span></span> <br/> |<span data-ttu-id="6bd2b-159">Dirección URL de este vínculo.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-159">The URL for this link.</span></span> <span data-ttu-id="6bd2b-160">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-160">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-161">**text**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-161">**text**</span></span> <br/> |<span data-ttu-id="6bd2b-162">Texto del vínculo que se mostrará en lugar de la dirección URL en sí.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-162">The link text to display instead of the URL itself.</span></span> <span data-ttu-id="6bd2b-163">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-163">Optional.</span></span>  <br/> |
   
### <a name="listvariable"></a><span data-ttu-id="6bd2b-164">listVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-164">listVariable</span></span>

|<span data-ttu-id="6bd2b-165">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-165">**Element**</span></span>|<span data-ttu-id="6bd2b-166">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-166">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-167">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-167">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-168">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-168">The name of the variable.</span></span> <span data-ttu-id="6bd2b-169">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-169">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-170">**listItems**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-170">**listItems**</span></span> <br/> |<span data-ttu-id="6bd2b-171">Un contenedor para los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-171">A container for items in the list.</span></span> <span data-ttu-id="6bd2b-172">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-172">Required.</span></span>  <br/> |
   
### <a name="picturevariable"></a><span data-ttu-id="6bd2b-173">pictureVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-173">pictureVariable</span></span>

|<span data-ttu-id="6bd2b-174">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-174">**Element**</span></span>|<span data-ttu-id="6bd2b-175">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-175">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-176">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-176">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-177">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-177">The name of the variable.</span></span> <span data-ttu-id="6bd2b-178">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-178">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-179">**value**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-179">**value**</span></span> <br/> |<span data-ttu-id="6bd2b-180">Dirección URL de la imagen.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-180">The URL for the picture.</span></span> <span data-ttu-id="6bd2b-181">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-181">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-182">**altText**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-182">**altText**</span></span> <br/> |<span data-ttu-id="6bd2b-183">Texto alternativo que se va a mostrar para accesibilidad y cuando el usuario mueve el puntero del mouse sobre la imagen.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-183">The alternate text to display for accessibility and when the user moves the mouse pointer over the picture.</span></span> <span data-ttu-id="6bd2b-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-184">Optional.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-185">**href**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-185">**href**</span></span> <br/> |<span data-ttu-id="6bd2b-186">El hipervínculo que se usará cuando el usuario haga clic en la imagen, si el destino deseado no es la dirección URL de imagen especificada por el **elemento de** valor.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-186">The hyperlink to use when the user clicks the picture, if the desired target is not the picture URL specified by the **value** element.</span></span> <span data-ttu-id="6bd2b-187">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-187">Optional.</span></span>  <br/> |
   
### <a name="publishervariable"></a><span data-ttu-id="6bd2b-188">publisherVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-188">publisherVariable</span></span>

|<span data-ttu-id="6bd2b-189">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-189">**Element**</span></span>|<span data-ttu-id="6bd2b-190">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-190">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-191">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-191">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-192">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-192">The name of the variable.</span></span> <span data-ttu-id="6bd2b-193">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-193">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-194">**id**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-194">**id**</span></span> <br/> |<span data-ttu-id="6bd2b-195">Identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-195">The unique ID of the user.</span></span> <span data-ttu-id="6bd2b-196">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-196">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-197">**nameHint**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-197">**nameHint**</span></span> <br/> |<span data-ttu-id="6bd2b-198">Nombre que se mostrará en el elemento de fuente.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-198">The name to be displayed in the feed item.</span></span> <span data-ttu-id="6bd2b-199">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-199">Optional.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-200">**profileUrl**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-200">**profileUrl**</span></span> <br/> |<span data-ttu-id="6bd2b-201">Dirección URL del perfil de la persona que se usará como hipervínculo para el nombre de la persona en el elemento de fuente, si el nombre de la persona está presente.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-201">The URL of the person's profile that will be used as the hyperlink for the person's name in the feed item, if the person's name is present.</span></span> <span data-ttu-id="6bd2b-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-202">Optional.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-203">**emailAddress**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-203">**emailAddress**</span></span> <br/> |<span data-ttu-id="6bd2b-204">La dirección de correo electrónico que se usa para actualizar la información de contacto de esta persona en Outlook.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-204">The email address that is used to update this person's contact information in Outlook.</span></span> <span data-ttu-id="6bd2b-205">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-205">Optional.</span></span>  <br/> |
   
### <a name="textvariable"></a><span data-ttu-id="6bd2b-206">textVariable</span><span class="sxs-lookup"><span data-stu-id="6bd2b-206">textVariable</span></span>

|<span data-ttu-id="6bd2b-207">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-207">**Element**</span></span>|<span data-ttu-id="6bd2b-208">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-208">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bd2b-209">**nombre**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-209">**name**</span></span> <br/> |<span data-ttu-id="6bd2b-210">El nombre de la variable.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-210">The name of the variable.</span></span> <span data-ttu-id="6bd2b-211">Necesario.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-211">Required.</span></span>  <br/> |
|<span data-ttu-id="6bd2b-212">**value**</span><span class="sxs-lookup"><span data-stu-id="6bd2b-212">**value**</span></span> <br/> |<span data-ttu-id="6bd2b-213">Texto que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-213">The text to display.</span></span> <span data-ttu-id="6bd2b-214">Opcional.</span><span class="sxs-lookup"><span data-stu-id="6bd2b-214">Optional.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bd2b-215">Consulte también</span><span class="sxs-lookup"><span data-stu-id="6bd2b-215">See also</span></span>

- [<span data-ttu-id="6bd2b-216">Información general sobre XML para un elemento de fuente de actividades</span><span class="sxs-lookup"><span data-stu-id="6bd2b-216">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)  
- [<span data-ttu-id="6bd2b-217">Elemento activityDetails</span><span class="sxs-lookup"><span data-stu-id="6bd2b-217">activityDetails Element</span></span>](activitydetails-element.md)  
- [<span data-ttu-id="6bd2b-218">Elemento activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="6bd2b-218">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)  
- [<span data-ttu-id="6bd2b-219">Directrices para mostrar actividades correctamente</span><span class="sxs-lookup"><span data-stu-id="6bd2b-219">Guidelines for Properly Displaying Activities</span></span>](guidelines-for-properly-displaying-activities.md)  
- [<span data-ttu-id="6bd2b-220">XML para actividades</span><span class="sxs-lookup"><span data-stu-id="6bd2b-220">XML for Activities</span></span>](xml-for-activities.md)  
- [<span data-ttu-id="6bd2b-221">Esquema XML del proveedor de Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="6bd2b-221">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)
- [<span data-ttu-id="6bd2b-222">Desarrollo de un proveedor con el esquema XML de OSC</span><span class="sxs-lookup"><span data-stu-id="6bd2b-222">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

