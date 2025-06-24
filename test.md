<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flex Containers with Inline CSS</title>
</head>
<body style="font-family: 'Inter', sans-serif; margin: 0; padding: 0; background-color: #f0f4f8; display: flex; justify-content: center; align-items: center; min-height: 100vh;">
    <div style="display: flex; flex-wrap: wrap; gap: 1rem; padding: 1rem; width: 100%; max-width: 1200px; box-sizing: border-box;">
        <!-- Container 1 -->
        <div style="flex: 1; padding: 1.5rem; border-radius: 0.5rem; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; background-color: #DBEAFE; color: #1E40AF;">
            <p style="font-weight: bold; font-size: 1.125rem;">
                Container 1: This is the first flexible box. It will take up equal space with others in a row.
            </p>
        </div>
        <div style="flex: 1; padding: 1.5rem; border-radius: 0.5rem; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; background-color: #D1FAE5; color: #065F46;">
            <p style="font-weight: bold; font-size: 1.125rem;">
                Container 2: Another flexible container, designed to adapt to screen size.
            </p>
        </div>
        <div style="flex: 1; padding: 1.5rem; border-radius: 0.5rem; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; background-color: #FEF3C7; color: #92400E;">
            <p style="font-weight: bold; font-size: 1.125rem;">
                Container 3: Each container has a distinct background for clear visual separation.
            </p>
        </div>
        <div style="flex: 1; padding: 1.5rem; border-radius: 0.5rem; box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06); display: flex; align-items: center; justify-content: center; text-align: center; min-height: 120px; background-color: #FEE2E2; color: #991B1B;">
            <p style="font-weight: bold; font-size: 1.125rem;">
                Container 4: On small screens, these will stack vertically; on larger screens, they'll be side-by-side.
            </p>
        </div>
    </div>
</body>
</html>
