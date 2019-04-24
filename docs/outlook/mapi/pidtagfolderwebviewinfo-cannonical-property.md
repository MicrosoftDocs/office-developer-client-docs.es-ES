---
title: Propiedad canónica PidTagFolderWebViewInfo Cannonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderWebViewInfo
api_type:
- HeaderDef
ms.assetid: 96ea23df-aa4f-4b3e-9663-e7db39f668c1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 70932e703511235e9f5e32efd95b18d1b66494e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316313"
---
# <a name="pidtagfolderwebviewinfo-cannonical-property"></a><span data-ttu-id="36a38-103">Propiedad canónica PidTagFolderWebViewInfo Cannonical Property</span><span class="sxs-lookup"><span data-stu-id="36a38-103">PidTagFolderWebViewInfo Cannonical Property</span></span>

  
  
<span data-ttu-id="36a38-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36a38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36a38-105">Contiene la dirección URL de la Página principal de una carpeta de Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="36a38-105">Contains the URL for the home page of a folder in Microsoft Outlook.</span></span> <span data-ttu-id="36a38-106">Esta propiedad contiene una secuencia binaria denominada **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="36a38-106">This property contains a binary stream called **WebViewPersistenceObject**.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36a38-107">Propiedades asociadas:</span><span class="sxs-lookup"><span data-stu-id="36a38-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="36a38-108">PR_FOLDER_WEBVIEWINFO</span><span class="sxs-lookup"><span data-stu-id="36a38-108">PR_FOLDER_WEBVIEWINFO</span></span>  <br/> |
|<span data-ttu-id="36a38-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="36a38-109">Identifier:</span></span>  <br/> |<span data-ttu-id="36a38-110">0x36DF</span><span class="sxs-lookup"><span data-stu-id="36a38-110">0x36DF</span></span>  <br/> |
|<span data-ttu-id="36a38-111">Tipo de datos:</span><span class="sxs-lookup"><span data-stu-id="36a38-111">Data type:</span></span>  <br/> |<span data-ttu-id="36a38-112">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="36a38-112">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="36a38-113">Área:</span><span class="sxs-lookup"><span data-stu-id="36a38-113">Area:</span></span>  <br/> |<span data-ttu-id="36a38-114">Carpeta MAPI</span><span class="sxs-lookup"><span data-stu-id="36a38-114">MAPI folder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36a38-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="36a38-115">Remarks</span></span>

<span data-ttu-id="36a38-116">Se puede especificar la dirección URL de una página principal para cualquier carpeta de Outlook.</span><span class="sxs-lookup"><span data-stu-id="36a38-116">A home page URL can be specified for any Outlook folder.</span></span> <span data-ttu-id="36a38-117">Se puede tener acceso a esta información en Outlook desde la ficha **Página principal** del cuadro de diálogo Propiedades de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="36a38-117">This information can be accessed in Outlook from the **Home Page** tab of the Properties dialog box for a folder.</span></span> 
  
<span data-ttu-id="36a38-118">En función de la configuración de la Directiva, es posible que Outlook omita la Página principal si el almacén MAPI que contiene esta carpeta no informa de MSCAP_SECURE_FOLDER_HOMEPAGES en su implementación de [IMSCapabilities:: GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) .</span><span class="sxs-lookup"><span data-stu-id="36a38-118">Depending on certain policy settings, the home page might be ignored by Outlook if the MAPI store that contains this folder does not report MSCAP_SECURE_FOLDER_HOMEPAGES in its [IMSCapabilities::GetCapabilities](pidtagfolderwebviewinfo-cannonical-property.md) implementation.</span></span> 
  
<span data-ttu-id="36a38-119">Tanto la carpeta **Outlook para hoy** como una carpeta pública pueden tener direcciones URL de la Página principal.</span><span class="sxs-lookup"><span data-stu-id="36a38-119">Both the **Outlook Today** folder and a public folder can have home page URLs.</span></span> <span data-ttu-id="36a38-120">Sin embargo, la carpeta **Outlook para hoy** utiliza un mecanismo diferente para administrar la dirección URL de la Página principal; ese mecanismo no se trata en este tema.</span><span class="sxs-lookup"><span data-stu-id="36a38-120">However the **Outlook Today** folder uses a different mechanism to manage its home page URL; that mechanism is not covered in this topic.</span></span> <span data-ttu-id="36a38-121">Una carpeta pública también puede tener definida una dirección URL de la Página principal que sea específica de un usuario.</span><span class="sxs-lookup"><span data-stu-id="36a38-121">A public folder might also have a home page URL defined in it that is specific to a user.</span></span> <span data-ttu-id="36a38-122">Sin embargo, esta funcionalidad no se describe en este tema.</span><span class="sxs-lookup"><span data-stu-id="36a38-122">However, that capability is not described in this topic.</span></span> 
  
<span data-ttu-id="36a38-123">El valor de esta propiedad es una secuencia binaria llamada **WebViewPersistenceObject**.</span><span class="sxs-lookup"><span data-stu-id="36a38-123">The value of this property is a binary stream called **WebViewPersistenceObject**.</span></span>
  
### <a name="webviewpersistenceobject-stream-structure"></a><span data-ttu-id="36a38-124">Estructura de la secuencia WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="36a38-124">WebViewPersistenceObject Stream Structure</span></span>

<span data-ttu-id="36a38-125">La estructura de la secuencia **WebViewPersistenceObject** contiene información sobre la dirección URL de una página principal de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="36a38-125">The **WebViewPersistenceObject** stream structure contains information about a home page URL for a folder.</span></span> 
  
<span data-ttu-id="36a38-126">Los elementos de datos de esta estructura se almacenan en el orden de bytes Little-endian, inmediatamente uno tras otro en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="36a38-126">Data elements in this structure are stored in little-endian byte order, immediately following one another in the following specified order.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="36a38-127">La siguiente descripción puede no mostrar todos los valores de campo compatibles con Outlook; por lo tanto, cuando el código Lee una secuencia existente, es posible que también se encuentren algunas marcas que no se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="36a38-127">The following description may not list all of the field values supported by Outlook; therefore, when your code reads an existing stream, some flags that are not listed here might also be found.</span></span> <span data-ttu-id="36a38-128">Sin embargo, puede usar esta descripción para crear mediante programación valores de la propiedad **PidTagFolderWebViewInfo** que Outlook entiende.</span><span class="sxs-lookup"><span data-stu-id="36a38-128">However, you can use this description to programmatically create values for the **PidTagFolderWebViewInfo** property that Outlook will understand.</span></span> 
  
 <span data-ttu-id="36a38-129">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="36a38-129">_dwVersion_</span></span>
  
> <span data-ttu-id="36a38-130">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="36a38-130">DWORD (4 bytes).</span></span> <span data-ttu-id="36a38-131">La versión del formato de la estructura.</span><span class="sxs-lookup"><span data-stu-id="36a38-131">The version of the structure's format.</span></span> <span data-ttu-id="36a38-132">A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="36a38-132">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="36a38-133">**Nombre del valor**</span><span class="sxs-lookup"><span data-stu-id="36a38-133">**Value name**</span></span>|<span data-ttu-id="36a38-134">**Value**</span><span class="sxs-lookup"><span data-stu-id="36a38-134">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36a38-135">WEBVIEW_PERSISTENCE_VERSION</span><span class="sxs-lookup"><span data-stu-id="36a38-135">WEBVIEW_PERSISTENCE_VERSION</span></span>  <br/> |<span data-ttu-id="36a38-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="36a38-136">0x00000002</span></span>  <br/> |
   
 <span data-ttu-id="36a38-137">_dwType_</span><span class="sxs-lookup"><span data-stu-id="36a38-137">_dwType_</span></span>
  
> <span data-ttu-id="36a38-138">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="36a38-138">DWORD (4 bytes).</span></span> <span data-ttu-id="36a38-139">Tipo de información de la Página principal.</span><span class="sxs-lookup"><span data-stu-id="36a38-139">The type of the home page information.</span></span> <span data-ttu-id="36a38-140">A partir de Microsoft Office Outlook 2007, el único valor admitido para este campo es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="36a38-140">As of Microsoft Office Outlook 2007, the only supported value for this field is as follows.</span></span>
    
|<span data-ttu-id="36a38-141">**Nombre del valor**</span><span class="sxs-lookup"><span data-stu-id="36a38-141">**Value name**</span></span>|<span data-ttu-id="36a38-142">**Value**</span><span class="sxs-lookup"><span data-stu-id="36a38-142">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36a38-143">WEBVIEWURL</span><span class="sxs-lookup"><span data-stu-id="36a38-143">WEBVIEWURL</span></span>  <br/> |<span data-ttu-id="36a38-144">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36a38-144">0x00000001</span></span>  <br/> |
   
 <span data-ttu-id="36a38-145">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="36a38-145">_dwFlags_</span></span>
  
> <span data-ttu-id="36a38-146">DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="36a38-146">DWORD (4 bytes).</span></span> <span data-ttu-id="36a38-147">Una combinación de cero o más indicadores cuyos valores y significados se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="36a38-147">A combination of zero or more flags whose values and meanings are listed in the following table.</span></span>
    
|<span data-ttu-id="36a38-148">Nombre de marca \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="36a38-148">\*\*\*\*Flag name\*\*\*\*</span></span>|<span data-ttu-id="36a38-149">\*\*\*\*Valor\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="36a38-149">\*\*\*\*Value\*\*\*\*</span></span>|<span data-ttu-id="36a38-150">\*\*\*\*Descripción\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="36a38-150">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36a38-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="36a38-151">WEBVIEW_FLAGS_SHOWBYDEFAULT</span></span>  <br/> |<span data-ttu-id="36a38-152">0x00000001</span><span class="sxs-lookup"><span data-stu-id="36a38-152">0x00000001</span></span>  <br/> |<span data-ttu-id="36a38-153">La casilla de verificación **Mostrar Página principal de forma predeterminada para esta carpeta** se activaba en la ficha **Página principal** del cuadro de diálogo Propiedades de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="36a38-153">The **Show home page by default for this folder** check box was checked in the **Home Page** tab of the Properties dialog box for a folder.</span></span>  <br/> |
   
 <span data-ttu-id="36a38-154">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="36a38-154">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="36a38-155">Una matriz de 7 elementos DWORD (total de 28 bytes).</span><span class="sxs-lookup"><span data-stu-id="36a38-155">An array of 7 DWORD elements (28 bytes total).</span></span> <span data-ttu-id="36a38-156">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="36a38-156">Unused.</span></span>
    
<span data-ttu-id="36a38-157">cbData</span><span class="sxs-lookup"><span data-stu-id="36a38-157">cbData</span></span>
  
> <span data-ttu-id="36a38-158">Un ULONG (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="36a38-158">A ULONG (4 bytes).</span></span> <span data-ttu-id="36a38-159">Tamaño, en bytes, del elemento de datos _wzURL_ .</span><span class="sxs-lookup"><span data-stu-id="36a38-159">The size, in bytes, of the  _wzURL_ data element.</span></span> 
    
 <span data-ttu-id="36a38-160">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="36a38-160">_wzURL_</span></span>
  
> <span data-ttu-id="36a38-161">Una matriz de elementos WCHAR.</span><span class="sxs-lookup"><span data-stu-id="36a38-161">An array of WCHAR elements.</span></span> <span data-ttu-id="36a38-162">Representación UTF-16 de la cadena de la dirección URL de la Página principal terminada en cero.</span><span class="sxs-lookup"><span data-stu-id="36a38-162">The UTF-16 representation of the zero-terminated home page URL string.</span></span>
    
### <a name="webviewpersistenceobject-stream-sample"></a><span data-ttu-id="36a38-163">Ejemplo de secuencia WebViewPersistenceObject</span><span class="sxs-lookup"><span data-stu-id="36a38-163">WebViewPersistenceObject Stream Sample</span></span>

<span data-ttu-id="36a38-164">En esta sección se describe un ejemplo de una secuencia **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="36a38-164">This section describes an example of a **WebViewPersistenceObject** stream.</span></span> <span data-ttu-id="36a38-165">La secuencia especifica la dirección URL de lahttps://www.microsoft.comPágina principal "".</span><span class="sxs-lookup"><span data-stu-id="36a38-165">The stream specifies the home page URL "https://www.microsoft.com".</span></span> 
  
 <span data-ttu-id="36a38-166">**Volcado de datos**</span><span class="sxs-lookup"><span data-stu-id="36a38-166">**Data dump**</span></span>
  
<span data-ttu-id="36a38-167">El siguiente es un volcado de datos de la secuencia tal como se mostraría en un editor binario.</span><span class="sxs-lookup"><span data-stu-id="36a38-167">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="36a38-168">**Desplazamiento de secuencia**</span><span class="sxs-lookup"><span data-stu-id="36a38-168">**Stream offset**</span></span>|<span data-ttu-id="36a38-169">**Bytes de datos**</span><span class="sxs-lookup"><span data-stu-id="36a38-169">**Data bytes**</span></span>|<span data-ttu-id="36a38-170">**Datos ASCII**</span><span class="sxs-lookup"><span data-stu-id="36a38-170">**ASCII data**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="36a38-171">0000000000</span><span class="sxs-lookup"><span data-stu-id="36a38-171">0000000000</span></span>  <br/> | `02 00 00 00 01 00 00 00 01 00 00 00 00 00 00 00` <br/> | `?...?...?.......` <br/> |
|<span data-ttu-id="36a38-172">0000000010</span><span class="sxs-lookup"><span data-stu-id="36a38-172">0000000010</span></span>  <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
|<span data-ttu-id="36a38-173">0000000020</span><span class="sxs-lookup"><span data-stu-id="36a38-173">0000000020</span></span>  <br/> | `00 00 00 00 00 00 00 00 32 00 00 00 68 00 74 00` <br/> | `........2...h.t.` <br/> |
|<span data-ttu-id="36a38-174">0000000030</span><span class="sxs-lookup"><span data-stu-id="36a38-174">0000000030</span></span>  <br/> | `74 00 70 00 3A 00 2F 00 2F 00 77 00 77 00 77 00` <br/> | `t.p.:././.w.w.w.` <br/> |
|<span data-ttu-id="36a38-175">0000000040</span><span class="sxs-lookup"><span data-stu-id="36a38-175">0000000040</span></span>  <br/> | `2E 00 6D 00 69 00 63 00 72 00 6F 00 73 00 6F 00` <br/> | `..m.i.c.r.o.s.o.` <br/> |
|<span data-ttu-id="36a38-176">0000000050</span><span class="sxs-lookup"><span data-stu-id="36a38-176">0000000050</span></span>  <br/> | `66 00 74 00 2E 00 63 00 6F 00 6D 00 00 00` <br/> | `f.t...c.o.m...` <br/> |
   
<span data-ttu-id="36a38-177">A continuación se muestra un análisis de los datos de ejemplo para la secuencia **WebViewPersistenceObject** .</span><span class="sxs-lookup"><span data-stu-id="36a38-177">The following is a parse of the sample data for the **WebViewPersistenceObject** stream.</span></span> 
  
 <span data-ttu-id="36a38-178">_dwVersion_</span><span class="sxs-lookup"><span data-stu-id="36a38-178">_dwVersion_</span></span>
  
> <span data-ttu-id="36a38-179">Offset 0X0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span><span class="sxs-lookup"><span data-stu-id="36a38-179">Offset 0x0, 4 bytes: 0x00000002 (WEBVIEW_PERSISTENCE_VERSION).</span></span>
    
 <span data-ttu-id="36a38-180">_dwType_</span><span class="sxs-lookup"><span data-stu-id="36a38-180">_dwType_</span></span>
  
> <span data-ttu-id="36a38-181">Desplazamiento 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span><span class="sxs-lookup"><span data-stu-id="36a38-181">Offset 0x4, 4 bytes: 0x00000001 (WEBVIEWURL).</span></span>
    
 <span data-ttu-id="36a38-182">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="36a38-182">_dwFlags_</span></span>
  
> <span data-ttu-id="36a38-183">Desplazamiento 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="36a38-183">Offset 0x8, 4 bytes: 0x00000001 (WEBVIEW_FLAGS_SHOWBYDEFAULT).</span></span>
    
 <span data-ttu-id="36a38-184">_dwUnused [7]_</span><span class="sxs-lookup"><span data-stu-id="36a38-184">_dwUnused[7]_</span></span>
  
> <span data-ttu-id="36a38-185">PosiciónInicial 0xC, 28 bytes: todo ceros.</span><span class="sxs-lookup"><span data-stu-id="36a38-185">Offset 0xC, 28 bytes: all zeros.</span></span>
    
 <span data-ttu-id="36a38-186">_cbData_</span><span class="sxs-lookup"><span data-stu-id="36a38-186">_cbData_</span></span>
  
> <span data-ttu-id="36a38-187">Desplazamiento 0x28, 4 bytes: 0x00000032.</span><span class="sxs-lookup"><span data-stu-id="36a38-187">Offset 0x28, 4 bytes: 0x00000032.</span></span>
    
 <span data-ttu-id="36a38-188">_wzURL_</span><span class="sxs-lookup"><span data-stu-id="36a38-188">_wzURL_</span></span>
  
> <span data-ttu-id="36a38-189">Desplazamiento 0x2C bytes: matriz de 25 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="36a38-189">Offset 0x2C, 0x32 bytes: array of 25 WCHARs.</span></span> <span data-ttu-id="36a38-190">Un valor de cadena terminada en cero Unicodehttps://www.microsoft.com: "".</span><span class="sxs-lookup"><span data-stu-id="36a38-190">A Unicode zero-terminated string value: "https://www.microsoft.com".</span></span>
    

