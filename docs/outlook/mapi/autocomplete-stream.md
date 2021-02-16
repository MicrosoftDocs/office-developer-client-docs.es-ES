---
title: Secuencia de Autocompletar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aadfba3e2674c35019a2e5f3eb374fbed1ad2a75
ms.sourcegitcommit: 0419850d5c1b3439d9da59070201fb4952ca5d07
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/28/2020
ms.locfileid: "49734227"
---
# <a name="autocomplete-stream"></a><span data-ttu-id="477ec-103">Secuencia de Autocompletar</span><span class="sxs-lookup"><span data-stu-id="477ec-103">Autocomplete Stream</span></span>

  
  
<span data-ttu-id="477ec-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="477ec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="477ec-105">Además de saber cómo Microsoft Outlook interactúa con la secuencia de autocompletar, también debe comprender el formato binario de la secuencia de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-105">In addition to knowing how Microsoft Outlook interacts with the autocomplete stream, you must also understand the binary format of the autocomplete stream.</span></span>
  
<span data-ttu-id="477ec-106">La secuencia de autocompletar es un conjunto de filas de la propiedad de destinatario que se guardan como una secuencia binaria con algunos metadatos de contabilidad que solo usan Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 y Microsoft Outlook 2003.</span><span class="sxs-lookup"><span data-stu-id="477ec-106">The autocomplete stream is a set of recipient property rows that are saved as a binary stream together with some bookkeeping metadata that is used only by Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007, and Microsoft Outlook 2003.</span></span> <span data-ttu-id="477ec-107">Los metadatos son relevantes para las interacciones de Outlook con el flujo de autocompletar, por lo que los terceros deben conservar el contenido de cada bloque de metadatos cuando guardan una secuencia de autocompletar modificada.</span><span class="sxs-lookup"><span data-stu-id="477ec-107">The metadata is relevant to Outlook interactions with the autocomplete stream so third parties must preserve what is in each metadata block when they save a modified autocomplete stream.</span></span> <span data-ttu-id="477ec-108">Dicho de otro modo, los terceros deben modificar solo la parte del conjunto de filas del formato binario y conservar el contenido que ya está en los bloques de metadatos de la secuencia de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-108">In other words, third parties should modify only the row-set part of the binary format and preserve what was already in the metadata blocks of the autocomplete stream.</span></span>
  
## <a name="stream-visualization"></a><span data-ttu-id="477ec-109">Visualización de flujo</span><span class="sxs-lookup"><span data-stu-id="477ec-109">Stream Visualization</span></span>

<span data-ttu-id="477ec-110">El diseño de alto nivel de la secuencia de autocompletar es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="477ec-110">The high-level layout of the autocomplete stream is as follows:</span></span>
  
<span data-ttu-id="477ec-111">Metadatos (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-111">Metadata (4 bytes)</span></span>
  
<span data-ttu-id="477ec-112">Número de versión principal (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-112">Major Version Number (4 bytes)</span></span>
  
<span data-ttu-id="477ec-113">Número de versión secundaria (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-113">Minor Version Number (4 bytes)</span></span>
  
<span data-ttu-id="477ec-114">Número de filas n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-114">Number of rows n (4 bytes)</span></span>
  
<span data-ttu-id="477ec-115">Número de propiedades p de la fila uno (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-115">Number of properties p in row one (4 bytes)</span></span>
  
<span data-ttu-id="477ec-116">Etiqueta de propiedad de la Propiedad 1 (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-116">Property 1's property tag (4 bytes)</span></span>
  
<span data-ttu-id="477ec-117">Datos reservados de la Propiedad 1 (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-117">Property 1's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="477ec-118">Unión de valor de la Propiedad 1 (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-118">Property 1's value union (8 bytes)</span></span>
  
<span data-ttu-id="477ec-119">Datos del valor de la Propiedad 1 (0 o bytes variables)</span><span class="sxs-lookup"><span data-stu-id="477ec-119">Property 1's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="477ec-120">…</span><span class="sxs-lookup"><span data-stu-id="477ec-120">…</span></span> <span data-ttu-id="477ec-121">(propiedades 2 por P-1)</span><span class="sxs-lookup"><span data-stu-id="477ec-121">(property 2 through property P-1)</span></span>
  
<span data-ttu-id="477ec-122">Etiqueta de la propiedad de la Propiedad p (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-122">Property p's property tag (4 bytes)</span></span>
  
<span data-ttu-id="477ec-123">Valor reservado de la Propiedad p (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-123">Property p's reserved data (4 bytes)</span></span>
  
<span data-ttu-id="477ec-124">Unión de valor de la Propiedad p (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-124">Property p's value union (8 bytes)</span></span>
  
<span data-ttu-id="477ec-125">Datos del valor de la Propiedad p (0 o bytes variables)</span><span class="sxs-lookup"><span data-stu-id="477ec-125">Property p's value data (0 or variable bytes)</span></span>
  
<span data-ttu-id="477ec-126">Número de propiedades q de la fila dos (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-126">Number of properties q in row two (4 bytes)</span></span>
  
<span data-ttu-id="477ec-127">…</span><span class="sxs-lookup"><span data-stu-id="477ec-127">…</span></span> <span data-ttu-id="477ec-128">(propiedades de la fila dos)</span><span class="sxs-lookup"><span data-stu-id="477ec-128">(row two's properties)</span></span>
  
<span data-ttu-id="477ec-129">…</span><span class="sxs-lookup"><span data-stu-id="477ec-129">…</span></span> <span data-ttu-id="477ec-130">(filas 3 a n-1)</span><span class="sxs-lookup"><span data-stu-id="477ec-130">(row 3 through row n-1)</span></span>
  
<span data-ttu-id="477ec-131">Número de propiedades p de la fila n (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-131">Number of properties r in row n (4 bytes)</span></span>
  
<span data-ttu-id="477ec-132">…</span><span class="sxs-lookup"><span data-stu-id="477ec-132">…</span></span> <span data-ttu-id="477ec-133">(propiedades de la fila n)</span><span class="sxs-lookup"><span data-stu-id="477ec-133">(row n's properties)</span></span>
  
<span data-ttu-id="477ec-134">EI de recuento de byte de información adicional (4 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-134">Extra information byte count EI (4 bytes)</span></span>
  
<span data-ttu-id="477ec-135">Información adicional (bytes EI)</span><span class="sxs-lookup"><span data-stu-id="477ec-135">Extra information (EI bytes)</span></span>
  
<span data-ttu-id="477ec-136">Metadatos (8 bytes)</span><span class="sxs-lookup"><span data-stu-id="477ec-136">Metadata (8 bytes)</span></span>
  
<span data-ttu-id="477ec-137">Para obtener un ejemplo de una estructura binaria, vea el ejemplo binario en las [Directrices de desarrollador y formato de archivo NK2 de Outlook 2003/2007.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span><span class="sxs-lookup"><span data-stu-id="477ec-137">For an example of a binary structure, see Binary Example in the [Outlook 2003/2007 NK2 File Format and Developer Guidelines.](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)</span></span>
  
## <a name="high-level-layout"></a><span data-ttu-id="477ec-138">Diseño de alto nivel</span><span class="sxs-lookup"><span data-stu-id="477ec-138">High-level Layout</span></span>

<span data-ttu-id="477ec-139">En términos generales, el diseño de la secuencia de autocompletar es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="477ec-139">Broadly speaking, the layout of the autocomplete stream is as follows:</span></span>
  
|<span data-ttu-id="477ec-140">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-140">**Value Data**</span></span>|<span data-ttu-id="477ec-141">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-141">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-142">Metadatos</span><span class="sxs-lookup"><span data-stu-id="477ec-142">Metadata</span></span>  <br/> |<span data-ttu-id="477ec-143">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-143">4</span></span>  <br/> |
|<span data-ttu-id="477ec-144">Número de versión principal</span><span class="sxs-lookup"><span data-stu-id="477ec-144">Major Version Number</span></span>  <br/> |<span data-ttu-id="477ec-145">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-145">4</span></span>  <br/> |
|<span data-ttu-id="477ec-146">Número de versión secundaria</span><span class="sxs-lookup"><span data-stu-id="477ec-146">Minor Version Number</span></span>  <br/> |<span data-ttu-id="477ec-147">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-147">4</span></span>  <br/> |
|<span data-ttu-id="477ec-148">Conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="477ec-148">Row-set</span></span>  <br/> |<span data-ttu-id="477ec-149">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-149">Variable</span></span>  <br/> |
|<span data-ttu-id="477ec-150">EI de recuento de byte de información adicional</span><span class="sxs-lookup"><span data-stu-id="477ec-150">Extra information byte count EI</span></span>  <br/> |<span data-ttu-id="477ec-151">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-151">4</span></span>  <br/> |
|<span data-ttu-id="477ec-152">Información adicional</span><span class="sxs-lookup"><span data-stu-id="477ec-152">Extra information</span></span>  <br/> |<span data-ttu-id="477ec-153">EI</span><span class="sxs-lookup"><span data-stu-id="477ec-153">EI</span></span>  <br/> |
|<span data-ttu-id="477ec-154">Metadatos</span><span class="sxs-lookup"><span data-stu-id="477ec-154">Metadata</span></span>  <br/> |<span data-ttu-id="477ec-155">8 </span><span class="sxs-lookup"><span data-stu-id="477ec-155">8</span></span>  <br/> |
   
<span data-ttu-id="477ec-156">Al leer esta secuencia, si la versión principal es diferente de 12, esta secuencia no debe leerse ni escribirse.</span><span class="sxs-lookup"><span data-stu-id="477ec-156">When reading this stream, if the major version is different than 12, then this stream should not be read or written.</span></span> <span data-ttu-id="477ec-157">La versión secundaria actual de la secuencia de autocompletar es 0, que tiene el recuento de byte de información adicional establecido en 0.</span><span class="sxs-lookup"><span data-stu-id="477ec-157">The current minor version of the autocomplete stream is 0, which has the Extra Information Byte count set to 0.</span></span> <span data-ttu-id="477ec-158">Si la versión secundaria es distinta de 0, habrá información en la información adicional que debe leerse al leer la secuencia y conservarse cuando se escribe la secuencia.</span><span class="sxs-lookup"><span data-stu-id="477ec-158">If the minor version is different than 0, then there will be information in the extra information that needs to be read when reading the stream and preserved when writing the stream.</span></span> <span data-ttu-id="477ec-159">La versión secundaria también deberá conservarse al escribir la secuencia.</span><span class="sxs-lookup"><span data-stu-id="477ec-159">The minor version will also need to be preserved when writing the stream.</span></span> <span data-ttu-id="477ec-160">Si no se conservan ambas, las instancias de Outlook que escribieron la información adicional perderán datos.</span><span class="sxs-lookup"><span data-stu-id="477ec-160">If both of these are not preserved, instances of Outlook that wrote the extra information will lose data.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="477ec-161">Las aplicaciones no deben agregar datos personalizados en el campo Información adicional o cambiar la versión secundaria, ya que esta funcionalidad admite las extensiones de Outlook en el formato y no extensiones arbitrarias de terceros.</span><span class="sxs-lookup"><span data-stu-id="477ec-161">Applications must not add custom data to the Extra Information field or change the minor version as this functionality is to support Outlook extensions to the format and not arbitrary third-party extensions.</span></span> 
  
## <a name="row-set-layout"></a><span data-ttu-id="477ec-162">Diseño del conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="477ec-162">Row-set Layout</span></span>

<span data-ttu-id="477ec-163">El diseño del conjunto de filas es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="477ec-163">The row-set layout is as follows:</span></span> 
  
|<span data-ttu-id="477ec-164">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-164">**Value Data**</span></span>|<span data-ttu-id="477ec-165">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-165">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-166">Número de filas</span><span class="sxs-lookup"><span data-stu-id="477ec-166">Number of rows</span></span>  <br/> |<span data-ttu-id="477ec-167">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-167">4</span></span>  <br/> |
|<span data-ttu-id="477ec-168">Filas</span><span class="sxs-lookup"><span data-stu-id="477ec-168">Rows</span></span>  <br/> |<span data-ttu-id="477ec-169">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-169">Variable</span></span>  <br/> |
   
<span data-ttu-id="477ec-170">El número de filas identifica cuántas filas tiene el siguiente elemento de la secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="477ec-170">The number of rows identifies how many rows come in the next part of the binary stream sequence.</span></span>
  
## <a name="row-layout"></a><span data-ttu-id="477ec-171">Diseño de fila</span><span class="sxs-lookup"><span data-stu-id="477ec-171">Row Layout</span></span>

<span data-ttu-id="477ec-172">Cada fila tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="477ec-172">Each row is of the following format:</span></span>
  
|<span data-ttu-id="477ec-173">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-173">**Value Data**</span></span>|<span data-ttu-id="477ec-174">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-174">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-175">Número de propiedades</span><span class="sxs-lookup"><span data-stu-id="477ec-175">Number of properties</span></span>  <br/> |<span data-ttu-id="477ec-176">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-176">4</span></span>  <br/> |
|<span data-ttu-id="477ec-177">Propiedades</span><span class="sxs-lookup"><span data-stu-id="477ec-177">Properties</span></span>  <br/> |<span data-ttu-id="477ec-178">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-178">Variable</span></span>  <br/> |
   
<span data-ttu-id="477ec-179">El número de propiedades identifica cuántas propiedades tiene el siguiente elemento de la secuencia binaria.</span><span class="sxs-lookup"><span data-stu-id="477ec-179">The number of properties identifies how many properties come in the next part of the binary stream sequence.</span></span>
  
## <a name="property-layout"></a><span data-ttu-id="477ec-180">Diseño de propiedad</span><span class="sxs-lookup"><span data-stu-id="477ec-180">Property Layout</span></span>

<span data-ttu-id="477ec-181">Cada propiedad tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="477ec-181">Each property is of the following format:</span></span>
  
|<span data-ttu-id="477ec-182">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-182">**Value Data**</span></span>|<span data-ttu-id="477ec-183">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-183">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-184">Etiqueta de propiedad</span><span class="sxs-lookup"><span data-stu-id="477ec-184">Property Tag</span></span>  <br/> |<span data-ttu-id="477ec-185">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-185">4</span></span>  <br/> |
|<span data-ttu-id="477ec-186">Datos reservados</span><span class="sxs-lookup"><span data-stu-id="477ec-186">Reserved Data</span></span>  <br/> |<span data-ttu-id="477ec-187">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-187">4</span></span>  <br/> |
|<span data-ttu-id="477ec-188">Unión de valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="477ec-188">Property Value Union</span></span>  <br/> ||
|<span data-ttu-id="477ec-189">Información del valor</span><span class="sxs-lookup"><span data-stu-id="477ec-189">Value Data</span></span>  <br/> |<span data-ttu-id="477ec-190">0 o variable (en función de la etiqueta de propiedad)</span><span class="sxs-lookup"><span data-stu-id="477ec-190">0 or variable (depending on the prop tag)</span></span>  <br/> |
   
## <a name="interpreting-the-property-value"></a><span data-ttu-id="477ec-191">Interpretar el valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="477ec-191">Interpreting the Property Value</span></span>

<span data-ttu-id="477ec-192">La unión de valor de propiedad y los datos de valor deben interpretarse en función de la etiqueta de propiedad de los 4 primeros bytes del bloque de propiedades.</span><span class="sxs-lookup"><span data-stu-id="477ec-192">The Property Value Union and the Value Data are to be interpreted based on the property tag in the first 4 bytes of the property block.</span></span> <span data-ttu-id="477ec-193">Esta etiqueta de propiedad está en el mismo formato que una etiqueta de propiedad MAPI.</span><span class="sxs-lookup"><span data-stu-id="477ec-193">This property tag is in the same format as a MAPI property tag.</span></span> <span data-ttu-id="477ec-194">Los bits de 0 a 15 de la etiqueta de propiedad son el tipo de propiedad.</span><span class="sxs-lookup"><span data-stu-id="477ec-194">Bits 0 through 15 of the property tag are the property's type.</span></span> <span data-ttu-id="477ec-195">Los bits de 16 a 31 son el identificador de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="477ec-195">Bits 16 through 31 are the property's identifier.</span></span> <span data-ttu-id="477ec-196">El tipo de propiedad determina cómo se debe leer el resto de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="477ec-196">The property type determines how the rest of the property should be read.</span></span>
  
## <a name="static-value"></a><span data-ttu-id="477ec-197">Valor estático</span><span class="sxs-lookup"><span data-stu-id="477ec-197">Static Value</span></span>

<span data-ttu-id="477ec-198">Algunas propiedades no tienen Datos de valor y solo tienen datos en la unión.</span><span class="sxs-lookup"><span data-stu-id="477ec-198">Some properties have no Value Data and only have data in the union.</span></span> <span data-ttu-id="477ec-199">Los siguientes tipos de propiedades (que proceden de la Etiqueta de propiedad) deben interpretar los datos de la unión de propiedad de 8 bytes como sigue:</span><span class="sxs-lookup"><span data-stu-id="477ec-199">The following property types (which come from the Property Tag) should interpret the 8-byte Property Union data as follows:</span></span>
  
|<span data-ttu-id="477ec-200">**Tipo de propiedad**</span><span class="sxs-lookup"><span data-stu-id="477ec-200">**Prop Type**</span></span>|<span data-ttu-id="477ec-201">**Interpretación de la unión de propiedad**</span><span class="sxs-lookup"><span data-stu-id="477ec-201">**Property Union Interpretation**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-202">PT_I2</span><span class="sxs-lookup"><span data-stu-id="477ec-202">PT_I2</span></span>  <br/> |<span data-ttu-id="477ec-203">short int</span><span class="sxs-lookup"><span data-stu-id="477ec-203">short int</span></span>  <br/> |
|<span data-ttu-id="477ec-204">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="477ec-204">PT_LONG</span></span>  <br/> |<span data-ttu-id="477ec-205">long</span><span class="sxs-lookup"><span data-stu-id="477ec-205">long</span></span>  <br/> |
|<span data-ttu-id="477ec-206">PT_ERROR</span><span class="sxs-lookup"><span data-stu-id="477ec-206">PT_ERROR</span></span>  <br/> |<span data-ttu-id="477ec-207">long</span><span class="sxs-lookup"><span data-stu-id="477ec-207">long</span></span>  <br/> |
|<span data-ttu-id="477ec-208">PT_R4</span><span class="sxs-lookup"><span data-stu-id="477ec-208">PT_R4</span></span>  <br/> |<span data-ttu-id="477ec-209">float</span><span class="sxs-lookup"><span data-stu-id="477ec-209">float</span></span>  <br/> |
|<span data-ttu-id="477ec-210">PT_DOUBLE</span><span class="sxs-lookup"><span data-stu-id="477ec-210">PT_DOUBLE</span></span>  <br/> |<span data-ttu-id="477ec-211">double</span><span class="sxs-lookup"><span data-stu-id="477ec-211">double</span></span>  <br/> |
|<span data-ttu-id="477ec-212">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="477ec-212">PT_BOOLEAN</span></span>  <br/> |<span data-ttu-id="477ec-213">short int</span><span class="sxs-lookup"><span data-stu-id="477ec-213">short int</span></span>  <br/> |
|<span data-ttu-id="477ec-214">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="477ec-214">PT_SYSTIME</span></span>  <br/> |<span data-ttu-id="477ec-215">FILETIME</span><span class="sxs-lookup"><span data-stu-id="477ec-215">FILETIME</span></span>  <br/> |
|<span data-ttu-id="477ec-216">PT_I8</span><span class="sxs-lookup"><span data-stu-id="477ec-216">PT_I8</span></span>  <br/> |<span data-ttu-id="477ec-217">LARGE_INTEGER</span><span class="sxs-lookup"><span data-stu-id="477ec-217">LARGE_INTEGER</span></span>  <br/> |
   
## <a name="dynamic-values"></a><span data-ttu-id="477ec-218">Valores dinámicos</span><span class="sxs-lookup"><span data-stu-id="477ec-218">Dynamic Values</span></span>

<span data-ttu-id="477ec-219">Otras propiedades tienen datos en un bloque de Datos del valor después de los primeros 16 bytes que contienen la Etiqueta de propiedad, los Datos reservados y la Unión de valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="477ec-219">Other properties have data in a Value Data block after the first 16 bytes that contain the Property Tag, the Reserved Data, and the Property Value Union.</span></span> <span data-ttu-id="477ec-220">A diferencia de los valores estáticos, los datos almacenados en la Unión de valor de propiedad de 8 bytes son irrelevantes al leer.</span><span class="sxs-lookup"><span data-stu-id="477ec-220">Unlike static values, the data that is stored in the 8-byte Property Value union is irrelevant on reading.</span></span> <span data-ttu-id="477ec-221">Al escribir, asegúrese de rellenar estos 8 bytes con algo.</span><span class="sxs-lookup"><span data-stu-id="477ec-221">When writing, make sure that you fill these 8 bytes with something.</span></span> <span data-ttu-id="477ec-222">Sin embargo, no es importante el contenido de los 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="477ec-222">However, the content of the 8 bytes is not important.</span></span> <span data-ttu-id="477ec-223">En los valores dinámicos, el tipo de etiqueta de propiedad determina cómo interpretar los Datos de valor.</span><span class="sxs-lookup"><span data-stu-id="477ec-223">In dynamic values, the property tag's type determines how to interpret the Value Data.</span></span>
  
<span data-ttu-id="477ec-224">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="477ec-224">PT_STRING8</span></span> 
  
|<span data-ttu-id="477ec-225">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-225">**Value Data**</span></span>|<span data-ttu-id="477ec-226">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-226">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-227">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="477ec-227">Number of bytes n</span></span>  <br/> |<span data-ttu-id="477ec-228">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-228">4</span></span>  <br/> |
|<span data-ttu-id="477ec-229">Bytes que se interpretarán como una cadena de ANSI (incluye terminador NULL)</span><span class="sxs-lookup"><span data-stu-id="477ec-229">Bytes to be interpreted as an ANSI string (includes NULL terminator)</span></span>  <br/> |<span data-ttu-id="477ec-230">n</span><span class="sxs-lookup"><span data-stu-id="477ec-230">n</span></span>  <br/> |
   
<span data-ttu-id="477ec-231">PT_CLSID</span><span class="sxs-lookup"><span data-stu-id="477ec-231">PT_CLSID</span></span>
  
|<span data-ttu-id="477ec-232">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-232">**Value Data**</span></span>|<span data-ttu-id="477ec-233">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-233">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-234">Bytes que se interpretarán como un GUID</span><span class="sxs-lookup"><span data-stu-id="477ec-234">Bytes to be interpreted as a GUID</span></span>  <br/> |<span data-ttu-id="477ec-235">16 </span><span class="sxs-lookup"><span data-stu-id="477ec-235">16</span></span>  <br/> |
|||
   
<span data-ttu-id="477ec-236">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="477ec-236">PT_BINARY</span></span> 
  
|<span data-ttu-id="477ec-237">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-237">**Value Data**</span></span>|<span data-ttu-id="477ec-238">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-238">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-239">Número de bytes n</span><span class="sxs-lookup"><span data-stu-id="477ec-239">Number of bytes n</span></span>  <br/> |<span data-ttu-id="477ec-240">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-240">4</span></span>  <br/> |
|<span data-ttu-id="477ec-241">Bytes que se interpretarán como una matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="477ec-241">Bytes to be interpreted as a byte array</span></span>  <br/> |<span data-ttu-id="477ec-242">n</span><span class="sxs-lookup"><span data-stu-id="477ec-242">n</span></span>  <br/> |
   
<span data-ttu-id="477ec-243">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="477ec-243">PT_MV_BINARY</span></span>
  
|<span data-ttu-id="477ec-244">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-244">**Value Data**</span></span>|<span data-ttu-id="477ec-245">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-245">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-246">Número de matrices binarias X</span><span class="sxs-lookup"><span data-stu-id="477ec-246">Number of binary arrays X</span></span>  <br/> |<span data-ttu-id="477ec-247">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-247">4</span></span>  <br/> |
|<span data-ttu-id="477ec-248">Una ejecución de bytes que contiene X matrices binarias.</span><span class="sxs-lookup"><span data-stu-id="477ec-248">A run of bytes that contains X binary arrays.</span></span> <span data-ttu-id="477ec-249">Cada matriz debe interpretarse exactamente igual al byte PT_BINARY ejecutado.</span><span class="sxs-lookup"><span data-stu-id="477ec-249">Each array should be interpreted exactly like the PT_BINARY byte run.</span></span>  <br/> |<span data-ttu-id="477ec-250">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-250">Variable</span></span>  <br/> |
   
<span data-ttu-id="477ec-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010 y Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="477ec-251">PT_MV_STRING8 (Outlook 2007, Outlook 2010, and Outlook 2013)</span></span>
  
|<span data-ttu-id="477ec-252">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-252">**Value Data**</span></span>|<span data-ttu-id="477ec-253">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-253">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-254">Número de cadenas ANSI X</span><span class="sxs-lookup"><span data-stu-id="477ec-254">Number of ANSI strings X</span></span>  <br/> |<span data-ttu-id="477ec-255">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-255">4</span></span>  <br/> |
|<span data-ttu-id="477ec-256">Una ejecución de bytes que contiene las cadenas ANSI X.</span><span class="sxs-lookup"><span data-stu-id="477ec-256">A run of bytes that contains X ANSI strings.</span></span> <span data-ttu-id="477ec-257">Cada cadena debe interpretarse exactamente igual al byte PT_STRING8 ejecutado.</span><span class="sxs-lookup"><span data-stu-id="477ec-257">Each string should be interpreted exactly like the PT_STRING8 byte run.</span></span>  <br/> |<span data-ttu-id="477ec-258">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-258">Variable</span></span>  <br/> |
   
<span data-ttu-id="477ec-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span><span class="sxs-lookup"><span data-stu-id="477ec-259">PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)</span></span>
  
|<span data-ttu-id="477ec-260">**Datos de valor**</span><span class="sxs-lookup"><span data-stu-id="477ec-260">**Value Data**</span></span>|<span data-ttu-id="477ec-261">**Número de bytes**</span><span class="sxs-lookup"><span data-stu-id="477ec-261">**Number of Bytes**</span></span>|
|:-----|:-----|
|<span data-ttu-id="477ec-262">Número de cadenas UNICODE X</span><span class="sxs-lookup"><span data-stu-id="477ec-262">Number of UNICODE strings X</span></span>  <br/> |<span data-ttu-id="477ec-263">4 </span><span class="sxs-lookup"><span data-stu-id="477ec-263">4</span></span>  <br/> |
|<span data-ttu-id="477ec-264">Una ejecución de bytes que contiene X cadenas UNICODE.</span><span class="sxs-lookup"><span data-stu-id="477ec-264">A run of bytes that contains X UNICODE strings.</span></span> <span data-ttu-id="477ec-265">Cada cadena debe interpretarse exactamente igual al byte PT_UNICODE ejecutado.</span><span class="sxs-lookup"><span data-stu-id="477ec-265">Each string should be interpreted exactly like the PT_UNICODE byte run.</span></span>  <br/> |<span data-ttu-id="477ec-266">Variable</span><span class="sxs-lookup"><span data-stu-id="477ec-266">Variable</span></span>  <br/> |
   
## <a name="significant-properties"></a><span data-ttu-id="477ec-267">Propiedades importantes</span><span class="sxs-lookup"><span data-stu-id="477ec-267">Significant properties</span></span>

<span data-ttu-id="477ec-268">Como se indicó anteriormente en este tema, los bloques binarios que representan las propiedades tienen etiquetas de propiedades que se corresponden a propiedades de los destinatarios de la libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="477ec-268">As mentioned previously in this topic, the binary blocks that represent properties have property tags that correspond to properties on address book recipients.</span></span> <span data-ttu-id="477ec-269">Para propiedades que no se muestran aquí, puede buscar la descripción de la propiedad en https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span><span class="sxs-lookup"><span data-stu-id="477ec-269">For properties that are not listed here, you can look up the property description at https://msdn.microsoft.com/library/cc433490(EXCHG.80).aspx.</span></span>
  
|<span data-ttu-id="477ec-270">**Nombre de propiedad**</span><span class="sxs-lookup"><span data-stu-id="477ec-270">**Property Name**</span></span>|<span data-ttu-id="477ec-271">**Etiqueta de propiedad**</span><span class="sxs-lookup"><span data-stu-id="477ec-271">**Property Tag**</span></span>|<span data-ttu-id="477ec-272">**Descripción (vea MSDN para obtener más información)**</span><span class="sxs-lookup"><span data-stu-id="477ec-272">**Description (see MSDN for more information)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="477ec-273">PR_NICK_NAME_W (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)</span><span class="sxs-lookup"><span data-stu-id="477ec-273">PR_NICK_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="477ec-274">0x6001001f</span><span class="sxs-lookup"><span data-stu-id="477ec-274">0x6001001f</span></span>  <br/> |<span data-ttu-id="477ec-275">Esta propiedad debe ser la primera en cada fila del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-275">This property must be first in each recipient row.</span></span> <span data-ttu-id="477ec-276">Actúa como un identificador de clave de la fila del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-276">It functionally serves as a key identifier for the recipient row.</span></span>  <br/> |
|<span data-ttu-id="477ec-277">PR_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="477ec-277">PR_ENTRYID</span></span>  <br/> |<span data-ttu-id="477ec-278">0x0FFF0102</span><span class="sxs-lookup"><span data-stu-id="477ec-278">0x0FFF0102</span></span>  <br/> |<span data-ttu-id="477ec-279">El identificador de entrada de la libreta de direcciones del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-279">The address book entry identifier for the recipient.</span></span>  <br/> |
|<span data-ttu-id="477ec-280">PR_DISPLAY_NAME_W</span><span class="sxs-lookup"><span data-stu-id="477ec-280">PR_DISPLAY_NAME_W</span></span>  <br/> |<span data-ttu-id="477ec-281">0x3001001F</span><span class="sxs-lookup"><span data-stu-id="477ec-281">0x3001001F</span></span>  <br/> |<span data-ttu-id="477ec-282">El nombre para mostrar del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-282">The recipient's display name.</span></span>  <br/> |
|<span data-ttu-id="477ec-283">PR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="477ec-283">PR_EMAIL_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="477ec-284">0x3003001F</span><span class="sxs-lookup"><span data-stu-id="477ec-284">0x3003001F</span></span>  <br/> |<span data-ttu-id="477ec-285">La dirección de correo electrónico del destinatario (por ejemplo, juanperez@contoso.com o /o=Contoso/OU=Foo/cn=Recipients/cn=juanperez)</span><span class="sxs-lookup"><span data-stu-id="477ec-285">The recipient's email address (e.g. johndoe@contoso.com or /o=Contoso/OU=Foo/cn=Recipients/cn=johndoe)</span></span>  <br/> |
|<span data-ttu-id="477ec-286">PR_ADDRTYPE_W</span><span class="sxs-lookup"><span data-stu-id="477ec-286">PR_ADDRTYPE_W</span></span>  <br/> |<span data-ttu-id="477ec-287">0x3002001F</span><span class="sxs-lookup"><span data-stu-id="477ec-287">0x3002001F</span></span>  <br/> |<span data-ttu-id="477ec-288">Tipo de dirección del destinatario (por ejemplo, SMTP o EX).</span><span class="sxs-lookup"><span data-stu-id="477ec-288">The recipient's address type (e.g. SMTP or EX).</span></span>  <br/> |
|<span data-ttu-id="477ec-289">PR_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="477ec-289">PR_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="477ec-290">0x300B0102</span><span class="sxs-lookup"><span data-stu-id="477ec-290">0x300B0102</span></span>  <br/> |<span data-ttu-id="477ec-291">La clave de búsqueda MAPI del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-291">The recipient's MAPI search key.</span></span>  <br/> |
|<span data-ttu-id="477ec-292">PR_SMTP_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="477ec-292">PR_SMTP_ADDRESS_W</span></span>  <br/> |<span data-ttu-id="477ec-293">0x39FE001f</span><span class="sxs-lookup"><span data-stu-id="477ec-293">0x39FE001f</span></span>  <br/> |<span data-ttu-id="477ec-294">La dirección de SMTP del destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-294">The recipient's SMTP address.</span></span>  <br/> |
|<span data-ttu-id="477ec-295">PR_DROPDOWN_DISPLAY_NAME_W (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)</span><span class="sxs-lookup"><span data-stu-id="477ec-295">PR_DROPDOWN_DISPLAY_NAME_W (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="477ec-296">0X6003001f</span><span class="sxs-lookup"><span data-stu-id="477ec-296">0X6003001f</span></span>  <br/> |<span data-ttu-id="477ec-297">La cadena para mostrar que aparece en la lista Autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-297">The display string that appears in the autocomplete list.</span></span>  <br/> |
|<span data-ttu-id="477ec-298">PR_NICK_NAME_WEIGHT (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)</span><span class="sxs-lookup"><span data-stu-id="477ec-298">PR_NICK_NAME_WEIGHT (not transmitted on recipients, specific to autocomplete stream only)</span></span>  <br/> |<span data-ttu-id="477ec-299">0x60040003</span><span class="sxs-lookup"><span data-stu-id="477ec-299">0x60040003</span></span>  <br/> |<span data-ttu-id="477ec-300">El peso de esta entrada de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-300">The weight of this autocomplete entry.</span></span> <span data-ttu-id="477ec-301">El peso se usa para determinar en qué orden se producen las entradas de autocompletar cuando coinciden con la lista autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-301">The weight is used to determine in what order autocomplete entries occur when matching the autocomplete list.</span></span> <span data-ttu-id="477ec-302">Se mostrarán las entradas con mayor peso antes que las entradas con un peso inferior.</span><span class="sxs-lookup"><span data-stu-id="477ec-302">Entries with higher weight will show before entries with lower weight.</span></span> <span data-ttu-id="477ec-303">Esta propiedad ordena la lista completa de autocompletar.</span><span class="sxs-lookup"><span data-stu-id="477ec-303">The complete autocomplete list is sorted by this property.</span></span> <span data-ttu-id="477ec-304">El peso disminuye periódicamente con el tiempo y aumenta cuando el usuario envía un correo electrónico a este destinatario.</span><span class="sxs-lookup"><span data-stu-id="477ec-304">The weight periodically decreases over time and increases when the user sends an email to this recipient.</span></span> <span data-ttu-id="477ec-305">Vea la descripción más adelante en este tema para obtener más información sobre esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="477ec-305">See the description later in this topic for more information about this property.</span></span>  <br/> |
   
<span data-ttu-id="477ec-306">PR_NICK_NAME_WEIGHT</span><span class="sxs-lookup"><span data-stu-id="477ec-306">PR_NICK_NAME_WEIGHT</span></span>
  
<span data-ttu-id="477ec-307">La propiedad PR_NICK_NAME_WEIGHT ordena el conjunto de filas de la secuencia de autocompletar en orden descendente y la secuencia de autocompletar siempre debe conservar esta característica ordenada.</span><span class="sxs-lookup"><span data-stu-id="477ec-307">The set of rows in the autocomplete stream is sorted in descending order by the PR_NICK_NAME_WEIGHT property and the autocomplete stream should always preserve this sorted characteristic.</span></span> <span data-ttu-id="477ec-308">Por lo tanto, los cambios realizados en el peso de una fila también deben asegurar que la posición de la fila mantiene el criterio de ordenación de un conjunto completo de filas.</span><span class="sxs-lookup"><span data-stu-id="477ec-308">Therefore, any changes to a row's weight should also ensure that the row's position maintains the sorted order of the complete set of rows.</span></span> <span data-ttu-id="477ec-309">Cualquier adición al conjunto de filas debe insertarse en la posición para mantener el orden correcto.</span><span class="sxs-lookup"><span data-stu-id="477ec-309">Any additions to the row-set should be inserted to the correct position to maintain the sorted order.</span></span>
  
<span data-ttu-id="477ec-310">El valor mínimo de este peso es 0x1 y el valor máximo es LONG_MAX.</span><span class="sxs-lookup"><span data-stu-id="477ec-310">The minimum value of this weight is 0x1 and the maximum value is LONG_MAX.</span></span> <span data-ttu-id="477ec-311">Otros valores para el peso se consideran no válidos.</span><span class="sxs-lookup"><span data-stu-id="477ec-311">Any other values for the weight are considered invalid.</span></span>
  
<span data-ttu-id="477ec-312">Cuando Outlook 2007 envía un correo o resuelve a un destinatario, aumentará el peso del destinatario en 0x2000.</span><span class="sxs-lookup"><span data-stu-id="477ec-312">When Outlook 2007 sends a mail to or resolves a recipient, it will increase that recipient's weight by 0x2000.</span></span>
  

