---
title: Configurar UDF en Excel Online en Office Online Server
manager: lindalu
ms.date: 12/03/2019
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funciones definidas por el usuario (UDF) en Excel Online en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: e1b005079c03ae3028ba6bf9ee1156c6ae2eae80
ms.sourcegitcommit: 007aa2ceb4f569201c3f4372de5c83b6c61f8875
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2020
ms.locfileid: "43102936"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="71b06-103">Configurar UDF en Excel Online en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="71b06-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="71b06-104">Use funciones definidas por el usuario (UDF) en Excel Online en Office Online Server para llamar a funciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="71b06-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="71b06-105">Las funciones definidas por el usuario (UDF) en Excel Online permiten llamar a funciones personalizadas escritas en código administrado mediante fórmulas en celdas.</span><span class="sxs-lookup"><span data-stu-id="71b06-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="71b06-106">Puede usar UDF para:</span><span class="sxs-lookup"><span data-stu-id="71b06-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="71b06-107">Llamar a funciones matemáticas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="71b06-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="71b06-108">Obtener datos de orígenes de datos personalizados en hojas de cálculo.</span><span class="sxs-lookup"><span data-stu-id="71b06-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="71b06-109">Llamar a los servicios web.</span><span class="sxs-lookup"><span data-stu-id="71b06-109">Call web services.</span></span>
    
<span data-ttu-id="71b06-110">Puede instalar archivos binarios UDF en una de dos ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="71b06-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="71b06-111">Un directorio local.</span><span class="sxs-lookup"><span data-stu-id="71b06-111">A local directory.</span></span> <span data-ttu-id="71b06-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="71b06-112">For example:</span></span> 
    
    <span data-ttu-id="71b06-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="71b06-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="71b06-114">La memoria caché global de ensamblados.</span><span class="sxs-lookup"><span data-stu-id="71b06-114">The global assembly cache.</span></span> <span data-ttu-id="71b06-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="71b06-115">For example:</span></span> 
    
    <span data-ttu-id="71b06-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="71b06-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="71b06-117">Haga referencia a la ubicación al crear una **definición New-OfficeWebAppsExcelUserDefinedFunction** en el Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="71b06-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="71b06-118">Office Online Server no admite UDF ubicadas en recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="71b06-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="71b06-119">Habilitar UDF en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="71b06-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="71b06-120">Cuando un administrador crea una nueva granja Office Web Apps Server mediante el cmdlet [new-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell, los ensamblados UDF se deshabilitan de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="71b06-120">When an administrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://docs.microsoft.com/powershell/module/officewebapps/new-officewebappsfarm?view=officewebapps-ps) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="71b06-121">El valor predeterminado de la **marca ExcelUdfsAllowed** es false.</span><span class="sxs-lookup"><span data-stu-id="71b06-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="71b06-122">Para habilitar las UDF, ejecute el siguiente comando Windows PowerShell en el Office Online Server, después de Office granja de servidores de Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="71b06-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="71b06-123">Crear definiciones de UDF en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="71b06-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="71b06-124">Después de habilitar las UDF, debe crear una definición para el binario que contiene las UDF.</span><span class="sxs-lookup"><span data-stu-id="71b06-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="71b06-125">Para crear una definición para el binario UDF en el Office Online Server, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction.**</span><span class="sxs-lookup"><span data-stu-id="71b06-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="71b06-126">Este cmdlet incluye los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="71b06-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="71b06-127">**Ensamblado**</span><span class="sxs-lookup"><span data-stu-id="71b06-127">**Assembly**</span></span>
    
- <span data-ttu-id="71b06-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="71b06-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="71b06-129">**Habilitar** (establecido en False de forma predeterminada)</span><span class="sxs-lookup"><span data-stu-id="71b06-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="71b06-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="71b06-130">**Description**</span></span>
    
<span data-ttu-id="71b06-131">En los ejemplos siguientes se muestra cómo crear las definiciones de UDF.</span><span class="sxs-lookup"><span data-stu-id="71b06-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="71b06-132">Después de crear la nueva referencia UDF, ejecute **iisreset** en el servidor para recoger la referencia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="71b06-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="71b06-133">Comandos Office Online Server udf Windows PowerShell adicionales</span><span class="sxs-lookup"><span data-stu-id="71b06-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="71b06-134">Use los siguientes cmdlets Windows PowerShell para trabajar con UDF:</span><span class="sxs-lookup"><span data-stu-id="71b06-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="71b06-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (sin parámetros obligatorios): devuelve una lista de definiciones udf configuradas en el Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="71b06-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="71b06-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (parámetro Identity requerido): establece las propiedades de las definiciones de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="71b06-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="71b06-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (parámetro Identity obligatorio): quita las definiciones de UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="71b06-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="71b06-138">Muestra de UDF</span><span class="sxs-lookup"><span data-stu-id="71b06-138">UDF sample</span></span>

<span data-ttu-id="71b06-139">El siguiente archivo de ejemplo proporciona un libro de ejemplo que usa una UDF y el binario UDF:</span><span class="sxs-lookup"><span data-stu-id="71b06-139">The following sample file provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="71b06-140">[BooleanDataType.xlsx: ](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx)un libro de ejemplo que usa una UDF</span><span class="sxs-lookup"><span data-stu-id="71b06-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="71b06-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="71b06-141">See also</span></span>

- [<span data-ttu-id="71b06-142">Configurar las opciones administrativas de Excel Online</span><span class="sxs-lookup"><span data-stu-id="71b06-142">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="71b06-143">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="71b06-143">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

